# Sample
import java.io.*;
import javax.servlet.*;
public class  FirstServlet extends GenericServlet
{
    public void  service(ServletRequest req,ServletResponse res)throws IOException,ServletException
    {
        try
        {
        String name=req.getParameter("nm");
        res.setContentType("text/html");
        PrintWriter pw=res.getWriter();
        pw.println("<html><body><h1 align='center'>Hello <font color='red'>"+name+"</font> Wlcome to hyderabad</h1></body></html>");
        }
        catch(Exception e)
        {
            System.err.println(e);
        }
    }
}
