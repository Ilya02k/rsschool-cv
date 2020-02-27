1. Ilya Kazlou
2. __Conctact.__ Phone number +375293631317, email: ilya02k@gmail.com, Telegram: kozlenok02, [vk](vk.com/karapzy). 
3. __Summary.__ My goal is become a good professional in my sphere. I wish  to get in my life a new friends, colleagues and impressions. I always look for new experience because I think that experience is one of main part of my life. It allows  to get better today then yesterday so challenges are not problem for me. I love people, so I visited as volunteer a few it-conferences, communication and change experience with other people is pleasure for me. I want to be developer because I love study and focus on current tasks and improve the word thanks to IT-solution. 
4. __Skils.__  I know a  basic principles of Object oriented and structural programming. I know C++, Java and C# and R( for Data Mining) from university. Current I study algorithms, Theory of Probability and Mathematical Statistics. I acquainted with Thread in Java. I can make graphics application. 
5. __Code examples(latest)__  
```
 package lab1os;

import java.util.List;
import java.io.*;
import java.util.*;

/**
 *
 * @author fpm.kozlov
 */
class MyThread extends Thread {  
    
    String command = "";
    
    MyThread( String name ) {        
        super(name);
    }   
    
    public List search(String template, String subString, String startDirectory, boolean deepSearch) throws Exception{
        List<String> results = new ArrayList<String>();
        String regex = toRegex(template);
        File f = new File(startDirectory);
        String[] files = f.list();
        if(!f.isDirectory() || files == null){
            throw new Exception("It isn't directory or bad directory");
        } else{
            Arrays.asList(files).forEach(fileName -> {
                File file = new File(startDirectory + "\\" + fileName);
                if(file.isFile() && satisfiesThePattern(fileName, regex, subString)){
                    results.add(fileName);
                } else if(file.isDirectory() && deepSearch){
                    comeDown(regex, subString, file, results);
                }
            });
        }
        return results;
    }

    private boolean satisfiesThePattern(String fileName, String regex, String subString){
        return fileName.matches(regex) && fileName.contains(subString);
    }

    private void comeDown(String regex, String subString, File startDirectory, List<String> results){
        String[] files = startDirectory.list();
        if(files != null){
            Arrays.asList(files).forEach(fileName -> {
                File file = new File(startDirectory + "\\" + fileName);
                if(file.isFile() && satisfiesThePattern(fileName, regex, subString)){
                    results.add(fileName);
                } else if(file.isDirectory()){
                    comeDown(regex, subString, file, results);
                }
            });
        }
    }

    private String toRegex(String str){
        return str.replaceAll("\\.", "\\.").replaceAll("\\*", ".*");
    }
    
    public void run() {          
        try { 
            MyFrame frame = new MyFrame();
            frame.setVisible(true);
        }             
        catch ( Exception e ) {                
            System.err.print("Error" + e);            
        }    
    } 
} 

public class Lab1OS {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here
        MyThread thread1 = new MyThread("Тред 1");
        thread1.start();
        MyThread thread2 = new MyThread("Тред 2");
        thread2.start();
        
    }
    
}

```
  
6. __Education__  At this moment I am in my second year at The Faculty of Applied Mathematics and Computer Science. My speciality is Acturial math( specialist in field of risks). I finished the introduction to Java in Stepic( online education platform), C++ ( from Yandex in coursera.org),  R for Data Mining ( in Stepic). And I know different mathematical disciplines such as Linear Algebra, Mathematical Analysis, Theory of Graphs and Сombinatorics.
7. __English__ I have studied English with tutor since  summer. My goal is fluent language.  My level is Intermediate. 
