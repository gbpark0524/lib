```Java
private String exceptionTryCatchFinally(String hello) {
    File file = new File(hello);
    FileInputStream fileInputStream = null;
    try {
        fileInputStream = new FileInputStream(file);
        int read = fileInputStream.read();// 데이터 1byte 읽기
        System.out.println("try block");
        return "method";
    } catch (FileNotFoundException e) {
        System.out.println("catch block");
        return "file not found";
    } catch (IOException e) {
        System.out.println("catch block"); 
        return "IOException";
    } finally {
        System.out.println("finally block");
        try {
            if(fileInputStream != null) {
                fileInputStream.close();
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```
