---
title: Initialisierungs- und Bereinigungscode mit dem InfoPath 2003-Objektmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, Bereinigungscode, InfoPath 2003-kompatible Formularvorlagen, Initialisierungscode
localization_priority: Normal
ms.assetid: 8d19e8fa-4e5c-40bb-ae89-7a552cc7914d
description: Standardmäßig enthält die "FormCode.cs" oder "FormCode.vb" erstellte Datei wird für ein Formularvorlagenprojekt, das mit InfoPath 2003 kompatibel ist den Quellcode für die Programmierlogik des Formulars. Die Vorlage für das Projekt erstellt eine Klasse in der Datei "FormCode.cs" oder "FormCode.vb" ähnlich wie die Klassen in den folgenden Beispielen, in dem Sie die Initialisierung und Bereinigungscode sowie Handler für Formularereignisse definieren können. Die Dateien "FormCode.cs" und "FormCode.vb" Anwenden einer Assembly-Ebene System.ComponentModel.DescriptionAttribute-Attribut, das die Klasse als einzige Klasse identifiziert, auf dem Ereignishandler implementiert sind. Das Attribut "InfoPathNamespace" (die vom Typ InfoPathNamespaceAttribute implementiert wird) wird auf eine Klasse innerhalb der Klasse verwendeten XML-DOM-Auswahl Namespaces identifiziert angewendet. Die Namespaces verwiesen wird, in der "InfoPathNamespace" werden von der InfoPath-Projektsystems verwaltet.
ms.openlocfilehash: 7111a8525b092998e21d4c267b5884f50fdb9777
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790758"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a>Initialisierungs- und Bereinigungscode mit dem InfoPath 2003-Objektmodell

Standardmäßig enthält die "FormCode.cs" oder "FormCode.vb" erstellte Datei wird für ein Formularvorlagenprojekt, das mit InfoPath 2003 kompatibel ist den Quellcode für die Programmierlogik des Formulars. Die Vorlage für das Projekt erstellt eine Klasse in der Datei "FormCode.cs" oder "FormCode.vb" ähnlich wie die Klassen in den folgenden Beispielen, in dem Sie die Initialisierung und Bereinigungscode sowie Handler für Formularereignisse definieren können. Die Dateien "FormCode.cs" und "FormCode.vb" Anwenden einer Assembly-Ebene **System.ComponentModel.DescriptionAttribute** -Attribut, das die Klasse als einzige Klasse identifiziert, auf dem Ereignishandler implementiert sind. Das Attribut **"InfoPathNamespace"** (die vom Typ [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) implementiert wird) wird auf eine Klasse innerhalb der Klasse verwendeten XML-DOM-Auswahl Namespaces identifiziert angewendet. Die Namespaces verwiesen wird, in der **"InfoPathNamespace"** werden von der InfoPath-Projektsystems verwaltet. 
  
Die FormCode-Klasse selbst bietet `_Startup` und `_Shutdown` Methoden, die verwendet werden, zum Ausführen von Initialisierungs- und Bereinigungscode Routinen für alle Komponenten, die zusätzlich zum standard InfoPath-Funktionalität erforderlich sind, während das Formular geöffnet ist. 
  
> [!IMPORTANT]
> Rufen Sie die Member des InfoPath-Objektmodells nicht innerhalb der `_Startup` und `_Shutdown` Methoden. Sie sollten initialisieren und nur Mitglieder der externe Komponenten in diesen Methoden aufrufen. 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-27-27'")]
    public partial class FormCode
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // You can add additional initialization code here.
        }
        public void _Shutdown()
        {
        }
    }
}
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
    ' The namespace prefixes defined in this attribute must remain synchronized with
    ' those in the form definition file (.xsf).
    <InfoPathNamespace( _
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-36-40'")> _
    Public Class FormCode
        Private thisXDocument As XDocument
        Private thisApplication As Application
        Public Sub _Startup(app As Application, doc As XDocument)
            thisXDocument = doc
            thisApplication = app
            ' You can add additional initialization code here.
        End Sub
        Public Sub _Shutdown()
        End Sub
    End Class
End Namespace
```

## <a name="the-startup-method"></a>_Startup (Methode)

Neben der Bereitstellung von eines Ort zum Schreiben von Code für die Initialisierung für zusätzliche Komponenten, die `_Startup` -Methode initialisiert die `thisXDocument` und `thisApplication` Variablen, die den Zugriff auf Member der [XDocument-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) und [Anwendung im Formularcode verwendet werden können ](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx)Klassen im InfoPath-Objektmodell. Der Code erforderlich sind, um die zwei Variablen initialisieren wird automatisch von der Projektvorlage generiert. 
  
```cs
    private XDocument thisXDocument;
    private Application thisApplication;
    public void _Startup(Application app, XDocument doc)
    {
        thisXDocument = doc;
        thisApplication = app;
        // You can add additional initialization code here.
    }
```

```vb
    Private thisXDocument As XDocument
    Private thisApplication As Application
    Public Sub _Startup(app As Application, doc As XDocument)
        thisXDocument = doc
        thisApplication = app
        ' You can add additional initialization code here.
    End Sub

```

Die folgenden Beispiele zeigen einen einfachen Ereignishandler für eine Schaltfläche, verwendet die `thisXDocument` Variable auf die [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode des [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Typs zugreifen. 
  
```cs
[InfoPathEventHandler(MatchPath="CTRL1_5", EventType=InfoPathEventType.OnClick)]
public void CTRL1_5_OnClick(DocActionEvent e)
{
    // Write your code here.
    thisXDocument.UI.Alert("Hello!");
}
```

```vb
<InfoPathEventHandler(MatchPath:="CTRL1_5", EventType:=InfoPathEventType.OnClick)> _
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
    ' Write your code here.
    thisXDocument.UI.Alert("Hello!")
End Sub
```

Informationen zum Erstellen eines ereignishandlers finden Sie unter [Hinzufügen einer Event Handler mithilfe des InfoPath 2003-Objektmodells](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="the-shutdown-method"></a>_ShutDown (Methode)

Die `_Shutdown` -Methode ist die letzte-Methode aufgerufen, wenn ein Formular geschlossen wird. Sie können in dieser Methode keinen Code schreiben, die zum Bereinigen oder Abschließen von im Formular verwendeten Komponenten erforderlich ist. 
  
```cs
    public void _Shutdown()
    {
    }
```

```vb
    Public Sub _Shutdown()
    End    Sub
```

## <a name="initialization-and-clean-up-code-example"></a>Beispiel für Initialisierungs- und Bereinigungscode

Das folgende Beispiel zeigt, wie Sie eine Verbindung mit einer Microsoft SQL Server-Datenbank initialisieren die `_Startup` Methode, und schließen Sie die Verbindung der `_Shutdown` Methode. In der Reihenfolge für das Beispiel ordnungsgemäß funktioniert müssen Sie zuerst einen Verweis auf die Assembly System.Data von .NET Framework festlegen, indem Sie im Menü **Projekt** auf **Verweis hinzufügen** klicken und anschließend die Komponente System.Data.dll auf **.NET** Registerkarte. Beachten Sie, dass auch die `using System.Data.SqlClient` (oder `Imports System.Data.SqlClient)` -Direktive am oberen Rand der Formularcodedatei zur Reduzierung der Tastaturbefehle hinzugefügt wurde. 
  
> [!NOTE]
> Benutzer eines InfoPath-Formulars, die Formularcode enthält, die mit einer SQL Server-Datenbank verbunden wird möglicherweise Sicherheitsberechtigungen abhängig von der Bereitstellung des Formulars und Codezugriffssicherheits-Richtlinie definiert ist. Weitere Informationen zur Sicherheit finden Sie unter [Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md)und [Über das Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md) . 
  
```cs
using System;
using System.Data.SqlClient;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the form. Do not
// modify.
[assembly: System.ComponentModel.DescriptionAttribute(
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
namespace Template1
{
    // The namespace prefixes defined in this attribute must remain synchronized with
    // those in the form definition file (.xsf).
    [InfoPathNamespace(
        "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-05T20-56-13'")]
    public partial class Template1
    {
        private XDocument    thisXDocument;
        private Application    thisApplication;
        private SqlConnection sqlConnect;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            // Initialize variable for SQL Server connection.
            sqlConnect= new SqlConnection("server=localhost;Trusted_Connection=yes;database=Northwind");
        }
        public void _Shutdown()
        {
            // Close SQL Server connection at shut down.
            sqlConnect.Close();
        }
    }
}
```

```vb
Imports System
Imports System.Data.SqlClient
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
Imports Microsoft.VisualBasic
' Office integration attribute. Identifies the startup class for the form. Do not
' modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _
    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
Namespace Template1
        ' The namespace prefixes defined in this attribute must remain synchronized with
        ' those in the form definition file (.xsf).
        <InfoPathNamespace( _
            "xmlns:my='http://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-08T18-47-33'")>        _
        Public Class Template1
            Private thisXDocument As XDocument
            Private thisApplication As Application
            Private sqlConnect As SqlConnection
            Public Sub _Startup(app As Application, doc As XDocument)
                thisXDocument = doc
                thisApplication = app
                ' Initialize variable for SQL Server connection.
                sqlConnect = New SqlConnection _("server=localhost;Trusted_Connection=yes;database=Northwind")
            End Sub
        Public Sub _Shutdown()
            ' Close SQL Server connection.
            sqlConnect.Close()
        End Sub
    End Class
End Namespace
```

## <a name="see-also"></a>Siehe auch



[Hinzufügen eines Ereignishandlers mit dem InfoPath 2003-Objektmodell](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

