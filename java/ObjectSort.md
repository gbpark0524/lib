```java
import java.io.Console;
import java.util.ArrayList;
import java.util.Comparator;
import java.util.List;
import java.util.stream.Collectors;

class Main {
  public static void main(String[] args) {
		final Comparator<Truck> compT = (p1, p2) -> Integer.compare( p1.getWeight(), p2.getWeight());
		Truck t1 = new Truck(2);
		Truck t2 = new Truck(4);
		Truck t3 = new Truck(3);
		List<Truck> list = new ArrayList<Truck>();
		list.add(t1);
		list.add(t2);
		list.add(t3);
		for (Truck t : list) {
			System.out.println(t);
		}
		List<Truck> list2 = list.stream()
			.sorted(compT).collect(Collectors.toList());

		for (Truck t : list2) {
			System.out.println(t.getWeight());
		}
  }

	static class Truck {
		int weight;
		int move;
		public Truck(int weight) {
		    this.weight = weight;
		}
		public int getWeight() {
			return weight;
		}
  }
}
```
