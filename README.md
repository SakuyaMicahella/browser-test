browser test

window.navigator.appName ��������� ��׼ȷ
window.navigator.userAgent �û������ַ��� ��ʾ�������Ϣ
window.navigator.platform �û�����ϵͳwin32 mac unix

�������̽������ȷ��
BrowserDetect.browser  ���������
BrowserDetect.version   ������汾
BrowserDetect.OS          ���������ϵͳ

������
navigator.plugins ��һ�����飬�洢������Ѿ���װ����������б�
window.navigator.plugins[i].name         �����
window.navigator.plugins[i].filename     �ļ���
window.navigator.plugins[i].description   ������Ϣ

����IE������Ƿ����ĳ���
function hasPlugin(name){
      var name = name.toLowerCase();
      for(var i=0; i<window.navigator.plugin.length; i++)
      {
            if(window.navigator.plugins[i].name.toLowerCase().indexOf(name) > -1)
            {
                      return true;  
            }
            else
            {
                      return false;
            }
      }
}

�ͻ��˼�⣺
1���������
����IE������޷�window.innerWidth��ȡ��ȷ���underfind
�Ϳ��ж��Ƿ񷵻�underfindȻ����ʹ���ʺ�IE��

2������� ������
ͨ��bug���
var box = {
    toString : function(){}
};
for(var o in box){
     alert(o);
}
����IE��һ��BUG��δ���򣬿��ж�IE 

3���û�������
window.navigator.userAgent  ��ʾ�������Ϣ�ַ���

������ĳ������棺�����Ű���ҳ�ͽ��������������
IE -- Trident     IE8 ���ֳ����ˣ�֮ǰ��δ����
Firefox -- Gecko
Opera -- Presto     �ɰ汾�����޷����ֳ�������
Chrome -- WebKit  WebKit��KHTML���������һ����֧�����������
Safari -- WebKit
Konqueror -- KHTML
