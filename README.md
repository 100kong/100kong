
public class Practice2 {
    public static int solution(String str) {
        int cnt=0,save=0;
        boolean bool=false;
        for(int i=0;i<str.length()/2;i++){
            char ch1=str.charAt(i);
            char ch2=str.charAt(str.length()-i-1);
            if(ch1==ch2) continue;
            else {save=i;bool=true; break;}
        }
        if(bool){
            for(int i=0;i<str.length()/2;i++){
                if(save==i) continue;
                char ch1=str.charAt(i);
                char ch2=str.charAt(str.length()-cnt-1);
                if(ch1==ch2){cnt++; continue;}
                else return 2;
            }
        }
        if(bool) return 1;
        else return 0;
    }

    public static int isPalindrome(int left, int right, char[] arr, int delCnt) {

        return 0;
    }

    public static void main(String[] args) {
        // Test code
        String[] str = {"abba", "summuus", "xabba", "xabbay", "comcom", "comwwmoc", "comwwtmoc"};
        System.out.println(solution("abba"));
        System.out.println(solution("summuus"));
        System.out.println(solution("xabba"));
        System.out.println(solution("xabbay"));
        System.out.println(solution("comcom"));
        System.out.println(solution("comwwmoc"));
        System.out.println(solution("comwwtmoc"));
    }
}
