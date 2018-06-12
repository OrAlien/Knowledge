## ����������硷�����£�Ӧ�ò㣨The Application  Layer��

* Copyright(C)Ф�Ķ�����@�����Ƽ���ѧ�Զ���ѧԺ

# 7 The Application Layer

7.1 DNS��the Domain Name System
7.2 Electronic Mail*
7.3 The World Wide Web

Application

�C running in network hosts in ��user space��
�C exchange messages to implement app
�C e.g., email, file transfer, the Web

Application-layer protocols

�C one ��piece�� of an app
�C define messages exchanged by apps and actions taken
�C use services provided by lower layer protocols

[1](Chapter07/1.png)

# 7.1 DNS��the Domain Name System����ϵͳ

7.1.1 The DNS Name Space
7.1.2 Domain Resource Records
7.1.3 Name Servers

## ����ԭ��

* ����������ַ(��IP)���ڼ��䣬Ӧ��ʹ�÷��ŵ�ַ��������www.ustb.edu.cn��ʾUSTB��IP��ַ��

* ���ǣ����籾����ʹ��IP��ַ�ģ������Ҫһ����ɶ���֮���໥ת���Ļ��ơ�

* �������ģ�Ƚ�Сʱ������ARPANET��ÿ̨����ֻ�����һ���ļ���UNIX��host�������ļ����г���������IP��ַ�Ķ�Ӧ��ϵ��

* �������ģ�ܴ�ʱ�����������Ͳ������ˣ���˲���������ϵͳDNS��Domain Name System����

## DNS����

* ����ϵͳ��һ�����εġ������������ϵͳ����ʹ�÷ֲ�ʽ���ݿ����ʵ�֡�

* Ϊ�˽�������Ӱ���IP��ַ��

�CӦ�ó�����Ҫ���ý�������resolver����
�C�������򱾵�DNS��������
�C����DNS��ѯ�����֣������ذ�����Ӧ��IP��ַ����Ӧ���ĸ���������
�C��������IP��ַ���ظ����÷���

* �������Ӧ����UDP����ʽ������

* ����IP��ַ��Ӧ�ó��������Ŀ�������TCP���ӣ����������UDP���ݰ�

# 7.1.1 The DNS Name Space���ֿռ�

* 250����������

* ��Щ���ֱ���һ�����ֳ�������Щ����ɱ��ٴλ��֣��Դ�����

* ����������Ϊͨ�õĺ͹���/���������֡�ÿ����������������ͻ������й���

* DNS�У�ÿ̨��������������ɡ�.�����ֿ����ַ����ִ�����ɵġ�����www.ustb.edu.cn.

* �����Ǵ�Сд�޹صģ���edu���͡�EDU����ͬ�������255���ַ���ÿ�����63���ַ���

* �������������

[2](Chapter07/2.png)

## Internet�������ṹ

��Ĳ���������Ƕ��㡢������㣻Ϊ��֤ȫ��������ͳһ�ԣ��������涨����������

������Internet��Դ�أ������Ķ�����������֯ģʽ���֣�

* Net ������֯��
* edu �������ţ�
* gov �������ţ�
* mil ���²��ţ�
* com ��ҵ��֯��
* org ��������֯��
* int ������֯

�������һ�������������Ե���ģʽ���֣�

* cn �й���
* jp �ձ���
* hk ��ۣ�
* fr ������
* uk Ӣ����

������Ϣ���Ľ�������Ĺ���Ȩ����ָ���Ĺ���������������������Ϊ��������������������������������������Ĺ���Ȩ�����������Ĺ��������

�й���������Ϣ���ĸ�������ҹ��Ķ����򣬽�cn���Ϊ�����������

* Net ����֧�����ģ�
* edu �������ţ�
* gov �������ţ�
* ac ���л�����
* com ��ҵ��֯��
* org ���ַ�Ӯ������֯��
* int ������֯��

## ��֯�ڵ�����

һ��һ����֯ӵ��һ����Ĺ���Ȩ���Ϳ��Ծ����Ƿ���Ҫ��һ�����ֲ�Ρ���ˣ�Internet��״��νṹ������������ʹ���κ�һ�����ӵ�Internet����������һ��ȫ��Ψһ������

����������һ���ʽ������.�ļ�����.��������.��������.��������

�й���������Ϣ����CNNIC�����ǽ��������Ķ�����edu�򣩵Ĺ���Ȩ�����й�����������CERNET�������ģ�CERNET�������Ľ�edu�򻯷�Ϊ��������򣬲����������������������ѧ��������������磬edu���µ�ustb�������Ƽ���ѧ������ustb��Ĺ���Ȩ���豱�ƴ�����������ġ�������������ֽ�ustb�򻮷ֳɶ���ļ��򣬽��ļ�����������������Ż�����

```www.ustb.edu.cn```

* EDU.CN��CN������USTB.EDU.CN��EDU.CN������
* ��һ����cn����ʾ�����й���
* �ڶ�����edu.cn����ʾ�����й��������ţ�
* ��������ustb.edu.cn����ʾ���й��������������ġ�Ӣ����дΪustb��ѧУ��
* Www�Ǹ�У԰���е�һ̨��������������

* ���򡱣�������ÿһ���������ı�ź͵㣻

# 7.1.2 ������Դ��¼

?��DNS�����ݿ�������Դ��¼����ʾ�������������Ϣ����Ӧ�ó��������������ʱ���õ��ı�����������Ӧ����Դ��¼��

?��Դ��¼��һ����Ԫʽ

Domain_name Time_to_live Class Type Value

[3](Chapter07/3.png)

# 7.1.3 ����������

? DNS�������ռ仮��Ϊ������ص�������(zone) ��ÿ�����򸲸��������ռ��һ���ֲ��������������������������������й���

? ÿ��������һ�������������������ɸ���������������������ı߽绮�����˹����õģ����磺edu.cn ustb.edu.cn��������ͬ�����򣬷ֱ��и��Ե�������������

[4](Chapter07/4.png)

## ����������������תΪ��ӦIP��ַ

? �����������ѯһ������ʱ�����Ƚ��ò�ѯ���ݸ���������������

? ����������ڱ��������������Ĺ�Ͻ��Χ���ڱ������ݿ��в��Ҹ�������Ӧ��IP��ַ��ֱ�ӻش������

? ��������е�������Զ�ˣ�����������������һ��Զ�̲�ѯ�����õ�����ѯ���������������������������̫æ�ˣ��÷������ظ�ѹ���˲�ѯ���𷽡�

[5](Chapter07/5.png)

���������㷨

-�ݹ��ѯ��recursive query�����Ӷ���ʼ������Ҫ�����ַ�����ϵͳһ�������ȫ�����֡���ַ�任��

-������ѯ��iterative query�����ӱ�������������ѯ��ʼ��ÿ������һ����������������У��������ķ�������

��������

-�ݹ������������Ҫ�ɷ���������е���

-�ظ�������������Ҫ����������������е���

# 7.2 Electronic Mail*

7.2.1 Architecture and Services
7.2.2 The User Agent
7.2.3 Message Formats
7.2.4 Message Transfer
7.2.5 Final Delivery

## �����ʼ�

�����ʼ���Ӧ��

E-mail����ΪInternet�û�֮�䷢�ͺͽ�����Ϣ�ṩ��һ�ֿ�ݡ����۵��ִ���ͨ���ֶ�

�����ʼ���ַ��Username@Hostname.Domain-name

?Username:�û����������û���������ʹ�õ��˺ţ�

?Hostname���û��������ڵ��ʼ�����������������

?Domain-name���ʼ����������ڵ�������

?��ĳ̨�ʼ�������������Ϊmail���÷�������������Ϊ```ustb.edu.cn```���ڸ÷���������һ���ʼ��û����û���Ϊ```wang```�����û��ĵ����ʼ���ַΪ```wang@mail.ustb.edu.cn```��

# 7.2.1 Architecture and Services

* �û����������û��Ķ��ͷ��͵����ʼ���һ��Ϊ�û����̣�

?�ʼ���������ʼ��������������ʼ���Դ�˷�����Ŀ�Ķˣ�һ��Ϊϵͳ�ĺ�̨���̣�����Э��SMTP

?���ʼ�����Э��SMTP��Simple Mail Transfer Protocol��

[6](Chapter07/6.png)

## �����ʼ�ϵͳ�ṩ�Ĺ���

?�����ʼ�ϵͳ�ṩ�Ļ�������

�C���ģ�ָ������Ϣ��ش���Ϣ�Ĺ��̣�

�C���䣺ָ����Ϣ�ӷ����ߴ����������ߣ�

�C���棺����Ϣ�ķ�������������Ϣ�����ߣ�

�C��ʾ��ʹ����Ӧ�Ĺ���������յ�����Ϣ��ʾ��������

�C���������߶Խ��յ�����Ϣ���д����洢/����/ת���ȵȡ�

?�����߼�����

�Cmailbox����������洢�ʼ���

�Cmailing list��

�C���ͣ�cc���������ȼ������ܡ�

�C�ݼٴ���

# 7.2.2 �û����������ʼ��Ķ�����

?��Ҫ����

�C���͵����ʼ�

?email��ַ�����磬```webmaster@ustc.edu.cn```

?mailing list�����磬```students@mail.ustc.edu.cn```

�C�Ķ������ʼ�

?�û�����������ʱ����û���mailbox��֪ͨ�û��Ƿ������ʼ���������ժҪ�Ե���ʾ�ʼ������⡢�����߼����ʼ���״̬��

�C���ӣ�gmail, outlook, 163, foxmail��

# 7.2.3 Message Formats

RFC 5322�����£���The Internet Message Format 
�ʼ����ŷ⡢����ͷ�ֶΡ�һ�����к��ʼ��幹�ɡ�

[7](Chapter07/7.png)

## MIME����;Internet�ʼ���չ

MIME��Multipurpose Internet Mail Extensions���������˶�ͼ����������Ƶ����ִ���ļ��ȵ�֧�֡�Ϊ���ͷ�ASCII����ʼ������˱������

[8](Chapter07/8.png)

# 7.2.4 Message Transfer

?INTERNETʹ�ü��ʼ�����Э��SMTP��ɵ����ʼ��Ľ�����

?��������

�C��Ϣ���������Դ��������Ŀ��������25�Ŷ˿�֮�佨��һ��TCP���ӣ�ʹ�ü��ʼ�����Э��SMTPЭ�����ͨ�ţ�
�C��TCP���ӽ�����֮����Ϊ�ͻ����ʼ����ͷ��ȴ���Ϊ���������ʼ����շ����ȴ�����Ϣ��
�C���������ȷ���׼�����յ�SMTP��Ϣ�������Լ��ı�ʶ��׼���ý����ʼ���
�C�ͻ������ʼ��ķ����˵�ַ�������˵ĵ�ַ��������ȷ�������˴��ں���ָʾ�ͻ������ʼ���
�C�ͻ������ʼ�������������ȷ��
�C��������ķ������֮���ͷ����ӡ�

[9](Chapter07/9.png)

# 7.2.5 ��󴫵�FinalDelivery

IMAP��The Internet Message Access Protocol

Internet�ʼ�����Э��

?To use IMAP, the mail server runs an IMAP server that listens to port 143.

?Theuser agent runs an IMAP client.

?The client connects to the server and begins toissue commands from those listed in Fig. 7-17.

## IMAP

IMAP�ǽ���ʹ�õ����ս���Э��POP3�ĸĽ��档POP3ͨ�����ʼ����ص�������ϣ����������ڷ������ϣ�ʹ�÷ǳ������㡣

?First, the client will start a secure transport if one is to be used (in order tokeep the messages and commands confidential), and then log in or otherwiseauthenticate itself to the server.

?there are many commands to list folders and messages, fetch messages or even parts of messages, mark messages with flags for later deletion, and organize messages into folders.

?IMAP has many other features, e.g.,

�Cto address mail by using attributes (e.g., give me the first message from Alice).
�Cto perform searches on the server to find the messages that satisfy certain criteria so that only those messages are fetched by the client.

[10](Chapter07/10.png)

# 7.3 The World Wide Web

7.3.1 Architectural Overview
7.3.2 Static Web Pages
7.3.3 Dynamic Web Pages and Web Applications
7.3.4 HTTP��The HyperText Transfer Protocol
7.3.5 The Mobile Web
7.3.6 Web Search

?WWW��World Wide Web�������ڷ��ʱ鲼��INTERNET�ϵ��໥������һ��ĳ��ı���һ�ֽṹ��ܡ�

?��ʷ

?�C1989�꣬���WWW��˼�������ŷ�޺��о�����CERN��
?�C1991�꣬��һ��ԭ����������Hypertext ��91������չʾ��
?�C1993�꣬��һ��ͼ�λ��������Mosaic��
?�C1994�꣬Andreessen����NETSCAPE��˾������WEB�Ŀͻ��ͷ��������������΢���IE�����������һ���������ս
?�C1994�꣬CERN��MIT��ͬ����WWW��̳���ƶ���ص�Э���׼��http://www.w3.org��

������뷨�ḻ��WWW���磬�������������ѧ������,
Mark Zuckerberg��ʼ����Facebookʱ��Harvardѧ��, Sergey Brin��Larry Page����Googleʱ��Stanfordѧ����

# 7.3.1 Architectural Overview

?WWW���ɻ���������һ�����ҳ���ɵģ���Щ��ҳ������ͨ�ı������ı�Hypertext���Լ�ͼ����Ƭ�ȹ��ɣ�

?�û�ͨ����Ϊ���������IE����������ۿ���ҳ�������ȡ�����������ҳ�����������������ı��͸�ʽ�������ȷ����ʾ������

?��ҳ�е��ı�����ָ����������ҳ����ָ���Ϊ��������Hyperlink�����ı�����Ϊ���ı������ᱻ�ر����ʾ���������»��ߣ����û���ѡ��˳������ӣ�������Ὣ�˳���������ָ����ҳȡ�أ�

?�����ı���ҳ�а�������������������ý��ʱ����ҳ����Ϊ�ǳ�ý��ġ������һ��ͨ����ҵİ�����������ʾ��Щ��ý����Ϣ��

?ÿһҳ��ץȡ����ͨ���������󵽷���������������ҳ���������Ϊ��Ӧ������Э��ΪHTTP���ı�����Э�顣

## Architectural Overview

[11](Chapter07/11.png)

## �ͻ���

?ʹ��URL��ͳһ��Դ��λ�������ҵ�Ŀ����ҳ�ġ�URL����������ɣ�

�CЭ�����ͣ�HTTP���ı�����Э�顢FTP��TELNET�ȣ���
�C��ҳ���ڻ�����DNS������
�C������ҳ���ļ����ơ�

�磺```http://www.cs.washington.edu/index.html```

?��ȡ�������ӵĲ��裺

�C�����ȷ��URL��
�Cͨ��DNS����IP��ַ��
�C����TCP���ӣ�
�C�����������HTTP����������ҳ��
�C������������ҳ��ΪHTTP��Ӧ��
�C�������ʾҳ�棬
�C�ͷ����ӡ�

## ĳЩ������URL����

[12](Chapter07/12.png)

## MIME����

[13](Chapter07/13.png)

## ��������

��������������ѭ����ִ�����²��裺

?�������Կͻ��ˣ����������TCP���ӣ�
?��ȡҳ���·�������������ļ������֣�
?��ȡ�ļ���ͨ���Ӵ����ϣ���
?���ļ����ݷ��͸��ͻ���
?�ͷ�TCP���ӡ�

## �������˴���������

[14](Chapter07/14.png)

## ��������

��������ÿ�������ʵ�ʴ�����̣�

?�����������ҳ�������
?ִ�жԸ�ҳ��ķ��ʿ���
?��黺��
?�Ӵ����ϻ�ȡ�����ҳ�������һ������ҳ��ĳ���
?ȷ����Ӧ�е����ಿ�֣�����Ҫ���͵�MIME���ͣ�
?����Ӧ���ظ��ͻ�
?�ڷ���������־������һ������

# 7.3.2 Static Web Pages

?WWW�Ļ����ǽ�ҳ��ӷ����������ͻ��ˡ�
?����򵥵���ʽ�У�web��ҳ���Ǿ�̬�ģ�����Ϊ�������ϵ��ļ���
?ÿ�α��ͻ��˻�ȡ����ʾ�ķ�ʽ��һ���ġ�

## HTML----���ı��������

?�����˸�ʽ������ʽ�����<b>��ʾ�������͵Ŀ�ʼ��<\b>��ʾ�������
?�����κ��ı��༭����дHTML�ĵ���Ҳ�������ִ�������ר�õ��ı��༭��������, ��Macromedia Dreamweaver��

## HTML----���ı�����������

[15](Chapter07/15.png)

## CSS�����ʽ��

���õؿ��Ƹ�ʽ��ͬһ��ʽ�ɱ������ҳӦ��

[16](Chapter07/16.png)

# 7.3.3 Dynamic Web Pages and Web Applications

WWW����Ӧ�ó��򼰷���

?�ڵ���������վ�����Ʒ
?����ͼ�����Ŀ
?������ͼ
?�Ķ��ͷ��͵����ʼ�
?����

## Dynamic Web Pages: ���ͼ����

[17](Chapter07/17.png)

?ֱ�ӷ���ҳ��
?ҳ���а���Ӧ�ó���

## �������˶�̬Webҳ������

�����������ܴ������ʹ��, ��ǰ����������õ���```http://widget.com/cgi-bin/order.cgi``` ��POST

���ֵ��͵Ĵ���̬ҳ������ķ�����

?�������ؽӿ�CGI (Common Gateway Interface)

-�ṩ�ӿڣ�����Web���������˳��򼰽ű�ͨ��
-��˳��򼰽ű�����������Ϣ������HTMLҳ����Ϊ��Ӧ
-ͨ���ýű����Կ�������Python, Ruby, Perl��
-���õĳ���(��order.cgi)ͨ������cgi-binĿ¼��

?��ҳ����Ƕ�������Ľű����÷�����ִ����Щ�ű�һ���������շ����ͻ���ҳ�棬�糬�ı�Ԥ������PHP��Hypertext Preprocessor��������������չ��php��ʶ����PHP��ҳ��

## �������˶�̬Webҳ�����ɣ�PHP

[18](Chapter07/18.png)

## �������˶�̬Webҳ������

������ѡ������

?Java������ҳ��JSP����PHP���ƣ�Java��д����չ��jsp

?�������ҳ�棨ASP.NET��,Microsoft�汾��Ӧ��.NET����PHP��JSP,����չ��aspx

## �ͻ��˶�̬Webҳ������

?PHP��CGI������Ӧ����ƶ��¼�����ֱ�����û��������б�Ҫ��HTMLǶ��ű�

?��Щ�ű����������ڿͻ���

?�������ֽ���ʽҳ��ļ���ͳ��Ϊ��̬HTML

?�����еĿͻ��˽ű�����ΪJavascript

## �ͻ��˶�̬Webҳ������: Javascript

[19](Chapter07/19.png)

## PHP��Javascript

[20](Chapter07/20.png)

## �ͻ��˶�̬Webҳ������

����������

?VBScript������VisualBasic

?Applet������Java���������Java�������Applet��Ƕ�뵽HTMLҳ���У���������JVM�����������ִ��

?Microsoft��ActiveX�ؼ�����һ�ֱ������x86����ָ��ĳ���

Asageneralrule,JavaScriptprogramsareeasiertowrite,Javaappletsexecutefaster,andActiveXcontrolsrunfastestofall.

## AJAX----�첽Javascript��XML

?�ͻ��˵Ľű�����Javascript��ͨ���ͷ������ϵĽű�ͨ�������������ؼ������������ʹ�ã���Щ��������ϳ�ΪAJAX----�첽Javascript��XML

?���ȫ���ܵ�Ӧ�ã���Google��gmail��Maps��Docs�Ⱦ���AJAX��д

?AJAX����һ�����ԣ�����һ����Ҫһ��Эͬ�����ļ�����������

1.HTML and CSS to present information as pages.
2.DOM (Document Object Model) to change parts of pages while theyare viewed.�ĵ�����ģ�ͣ����ʱ�ɸı䲿��ҳ��
3.XML (eXtensible Markup Language) to let programs exchange applicationdata with the server.����չ�������
4.An asynchronous way for programs to send and retrieve XML data.
5.JavaScript as a language to bind all this functionality together.

## �ĵ�����ģ��DOM

[21](Chapter07/21.png)

## ����չ�������XML

?HTML�����ݼ���ʽ�����һ�𣬹�ע������Ϣ�ı�ʾ

?���WebӦ�ó�����Ҫ�������Ľṹ�����ݴ����ı�ʾ�з��뿪��

?XML��һ��˵���ṹ�����ݵ�����

?XMLû�ж����κα�ǩ���û����Զ����Լ��ı�ǩ

* XML�е��ֶο��Խ�һ������

[23](Chapter07/23.png)

?XML���ױ��������

?HTMLҲ�ɰ���XML���������壬�÷�����Ϊ��չ���ı��������XHTML

?XML����������֮�������ͨ�����ԣ�������ͨ����HTTPЭ�����ʱ���ͱ���Ϊһ��Web����WebService��

?�򵥶������Э��SOAP (Simple ObjectAccess Protocol)��һ��ʵ������������ϵͳ�޹ص�Web����ķ�����

The client just constructsthe request as an XML message and sends it to the server, using the HTTPprotocol. The server sends back a reply as an XML-formatted message. In thisway, applications on heterogeneous platforms can communicate.

## �������ɶ�̬ҳ��Ĳ�ͬ����

[24](Chapter07/24.png)

# 7.3.4 HTTP��The HyperText Transfer Protocol

?HTTP��һ��Ӧ�ò�Э�飬������TCP֮�ϣ�������Web�������

?HTTPԽ��Խ��һ�������Э�飬��֧�ֶ���Ӧ�ò������ý�岥�����������ͨ�Ų�����ר����Ϣ��

## HTTP������

[25](Chapter07/25.png)

## HTTP�ķ�����֧�ֵĲ��� �� HTTP�Ļ���

[26](Chapter07/26.png)

# 7.3.5�ƶ�Web

Compared to desktop computers, mobile phones presentseveral difficulties for Web browsing:

?Small screens preclude large pages and large images.
?Limited input capabilities make it tedious to enter URLs or otherlengthy input.
?Network bandwidth is limited over wireless linksand expensive, particularly on cellular(3G) networks.
?Connectivity may be intermittent.
?Computing power is limited, for reasons of battery life, size, heatdissipation, and cost.

## �ƶ�Web

?The approach that is increasingly used is to run the same Web protocols for mobiles and desktops, and to have Web sites deliver mobile-friendly content when the user happens to be on a mobile device.
?Web servers are able to detect whether to return desktop or mobile versions of Web pages by looking at the request headers.
?Thus, when a Web server receives a request, it may look at the headers and return a page with small images, less text, and simpler navigation to an iPhone and a full-featured page to an user on a laptop.
