---
title: Threadunterstützung in InfoPath-Projekten mit dem InfoPath 2003-Objektmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Multithreading [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen, Threading [InfoPath 2007], Unterstützung für Projekte mit InfoPath 2003-Objektmodell, InfoPath 2003-kompatible Formularvorlagen, Threading-Unterstützung
localization_priority: Normal
ms.assetid: f269d64d-4102-426d-be8e-d2742a993524
description: Die COM-Objekte, auf die über die Microsoft. Office. Interop. InfoPath. dll, Microsoft. Office. Interop. InfoPath. SemiTrust. dll und Microsoft. Office. Interop. InfoPath. Xml. dll-Interop-Assemblys zugegriffen wird, die von Microsoft InfoPath installiert werden, unterstützen keine Anrufe wird für mehrere Threads ausgeführt. Hierzu gehören die Schnittstellen für Microsoft XML Core Services (MSXML)-Objekte, die vom Microsoft. Office. Interop. InfoPath. SemiTrust-Namespace umschlossen werden (die meisten haben Namen, die mit IXMLDOM vorangestellt werden) und alle Schnittstellen, die von der Microsoft. Office. Interop. InfoPath. XML-Namespace, von denen keiner threadsicher ist.
ms.openlocfilehash: 1be2bd0181c47097440af54f1aa804a4f17b30bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299839"
---
# <a name="threading-support-in-infopath-projects-using-the-infopath-2003-object-model"></a>Threadunterstützung in InfoPath-Projekten mit dem InfoPath 2003-Objektmodell

Die COM-Objekte, auf die über die Microsoft. Office. Interop. InfoPath. dll, Microsoft. Office. Interop. InfoPath. SemiTrust. dll und Microsoft. Office. Interop. InfoPath. Xml. dll-Interop-Assemblys zugegriffen wird, die von Microsoft InfoPath installiert werden, unterstützen keine Anrufe wird für mehrere Threads ausgeführt. Hierzu gehören die Schnittstellen für Microsoft XML Core Services (MSXML)-Objekte, die vom **Microsoft. Office. Interop. InfoPath. SemiTrust** -Namespace umschlossen werden (die meisten haben Namen, die mit IXMLDOM vorangestellt werden) und alle Schnittstellen, die von der [Microsoft. Office. Interop. InfoPath. XML](https://msdn.microsoft.com/library/microsoft.office.interop.infopath.xml) -Namespace, von denen keiner threadsicher ist. 
  
Alle Aufrufe dieser COM-Objekte müssen auf einem einzigen Thread ausgegeben werden. Mit verwaltetem Code in einem InfoPath-Projekt können weitere Threads für die Ausführung von Hintergrundarbeiten erstellt werden. Code, der auf anderen Threads als dem Hauptthread ausgeführt wird, kann jedoch keine InfoPath-Objektmodelle aufrufen.
  
Wenn das InfoPath-Projekt mit verwaltetem Code mehrere Threads verwendet, müssen Sie bei der gemeinsamen Nutzung von Objekten zwischen Threads vorsichtig sein. Es sollten keine Verweise auf das XML-DOM (Document Object Model) oder Verweise auf InfoPath-Objekte zwischen Threads gemeinsam genutzt werden.  
  
## <a name="making-asynchronous-calls-to-the-infopath-object-model"></a>Senden von asynchronen Aufrufen an das InfoPath-Objektmodell

In Situationen, in denen ein Prozess, wie z. B. ein auf einem separaten Thread ausgeführter Zeitgeber, aufgerufen werden muss, lässt sich die Tatsache umgehen, dass das InfoPath-Objektmodell keine derartigen Aufrufe unterstützt.  
  
Im folgenden Beispiel wird in der _Startup-Methode des Formulars eine **System. Timers. Timer** -Instanz erstellt und ein asynchroner Rückruf an den Zeitgeber angeschlossen. Darüber hinaus wird eine unsichtbare Instanz des Fenster Formulars (**System. Windows. Forms. Form**) erstellt. Wenn die Rückruffunktion Timed verstrichen einmal pro Sekunde ausgeführt wird, wird die **** Win32-postmessagefunktion aufgerufen, um eine Nachricht im unsichtbaren Fenster zu veröffentlichen. Das unsichtbare Fenster verfügt über eine **WndProc** -Funktion, die die von der Timer-Rückruffunktion empfangene Nachricht verarbeitet und das XML-DOM (Document Object Model) des Formulars aktualisiert. Dieses Formular muss als voll vertrauenswürdiges Formular zum Ausführen installiert werden. Informationen zum Debuggen einer voll vertrauenswürdigen Formularvorlage finden Sie unter [Vorschau und Debuggen von Formularvorlagen, die volle VertrauenswürdigKeit erfordern](how-to-preview-and-debug-form-templates-that-require-full-trust.md). Informationen zum Bereitstelleneiner voll vertrauenswürdigen Formularvorlage finden Sie unter [Bereitstellen von InfoPath-Formularvorlagen mit Code](how-to-deploy-infopath-form-templates-with-code.md).
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
using System.Timers;
using System.Runtime.InteropServices;
// Office integration attribute. Identifies the startup class for the
// form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute("InfoPathStartupClass, Version=1.0, Class=AsyncUpdate.AsyncUpdate")]
namespace AsyncUpdate
{
    public class User32
    {
        [DllImport("User32.dll")]
        public static extern Int32 PostMessage(
            IntPtr hWnd, int Msg, int wParam, int lParam);
        public User32()
        {    
        }
        ~User32()
        {
        }
    }
    public class MyWindow : System.Windows.Forms.Form
    {
        private XDocument thisXDocument;
        private AsyncUpdate thisProcess ;
        // Private message for internal class.
        public const int WM_MYNOTIFY = 0x400;
        public MyWindow(XDocument doc, AsyncUpdate process)
        {
            thisXDocument = doc;
            thisProcess  = process;
            this.Text = "MyWindow";
            // Force HWND to get created in Win32
            IntPtr hwnd = this.Handle; 
        }
        [System.Security.Permissions.PermissionSet(System.Security.Permissions.SecurityAction.Demand, Name="FullTrust")]
        protected override void WndProc(
            ref System.Windows.Forms.Message m) 
        {
            switch (m.Msg)
            {
            case WM_MYNOTIFY:
                IXMLDOMNode xml = thisXDocument.DOM.selectSingleNode(
                    "/my:myFields/my:field1");
                xml.text = thisProcess.counter.ToString();
                break;                
            }
            base.WndProc(ref m);
        }
    }
    // The namespace prefixes defined in this attribute must remain 
    // synchronized with those in the form definition file (.xsf).
    [InfoPathNamespace("xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-02-11T23-29-59'")]
    public class AsyncUpdate
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public int counter;
        private System.Timers.Timer myTimer;
        private MyWindow myWnd;
    
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // init the counter
            counter = 0;
            // Start a timer on another thread
            myTimer = new System.Timers.Timer(1000);
            myTimer.Elapsed += new ElapsedEventHandler(
                myTimer_Elapsed);
            myTimer.Start();
            // create hidden window to receive notifications 
            // back on the main thread
            myWnd = new MyWindow(thisXDocument, this);
        }
        public void _Shutdown()
        {
            myWnd.Dispose();
            myTimer.Stop();
            myTimer.Dispose();
        }
        private void myTimer_Elapsed(object sender, ElapsedEventArgs e)
        {
            // This method is called on a second thread
            counter ++;
            // Post message back to main thread
            User32.PostMessage(
                myWnd.Handle, MyWindow.WM_MYNOTIFY, 0, 0);
        }
    }
}

```


