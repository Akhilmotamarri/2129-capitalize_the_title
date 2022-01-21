# 2129-capitalize_the_title
java
class Solution {
    public String capitalizeTitle(String title) {
       String ans="";
       String[] nstr=title.split(" ");
	for(int i=0;i<nstr.length;i++){
		    if(nstr[i].length()==1 || nstr[i].length()==2){
		        nstr[i]=nstr[i].toLowerCase();
		    }
		    else{		       
		        String temp=nstr[i];
                    nstr[i]=temp.substring(0,1).toUpperCase()+temp.substring(1,temp.length()).toLowerCase();	 
		    }
            ans=ans+nstr[i]+" ";
        }
        return ans.strip();
    }
}
