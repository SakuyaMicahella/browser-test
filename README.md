# browser test
window.navigator.appName ��������� ��׼ȷ<br/>
window.navigator.userAgent �û������ַ��� ��ʾ�������Ϣ<br/>
window.navigator.platform �û�����ϵͳwin32 mac unix<br/>

�������̽������ȷ��<br/>
BrowserDetect.browser  ���������<br/>
BrowserDetect.version   ������汾<br/>
BrowserDetect.OS          ���������ϵͳ<br/>

������<br/>
navigator.plugins ��һ�����飬�洢������Ѿ���װ����������б�<br/>
window.navigator.plugins[i].name         �����<br/>
window.navigator.plugins[i].filename     �ļ���<br/>
window.navigator.plugins[i].description   ������Ϣ<br/>

����IE������Ƿ����ĳ���<br/>
``` python
function hasPlugin(name){<br/>
      var name = name.toLowerCase();<br/>
      for(var i=0; i<window.navigator.plugin.length; i++)
      {
            if(window.navigator.plugins[i].name.toLowerCase().indexOf(name) > -1)
            {
                      return true;  
            }
            else
            {
                      return false;}
      }<br/>
}
```
<br/>
�ͻ��˼�⣺<br/>
�������<br/>
����IE������޷�window.innerWidth��ȡ��ȷ���underfind<br/>
�Ϳ��ж��Ƿ񷵻�underfindȻ����ʹ���ʺ�IE��<br/><br/>


�û�������<br/>
window.navigator.userAgent  ��ʾ�������Ϣ�ַ���<br/><br/>

������ĳ������棺�����Ű���ҳ�ͽ��������������<br/>
IE -- Trident     IE8 ���ֳ����ˣ�֮ǰ��δ����<br/>
Firefox -- Gecko<br/>
Opera -- Presto     �ɰ汾�����޷����ֳ�������<br/>
Chrome -- WebKit  WebKit��KHTML���������һ����֧�����������<br/>
Safari -- WebKit<br/>
Konqueror -- KHTML<br/>
