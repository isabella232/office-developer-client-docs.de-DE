---
title: Initialisierungs- und Bereinigungscode mit dem InfoPath 2003-Objektmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- InfoPath 2003-kompatible Formularvorlagen, Bereinigungscode, InfoPath 2003-kompatible Formularvorlagen, Initialisierungscode
localization_priority: Normal
ms.assetid: 8d19e8fa-4e5c-40bb-ae89-7a552cc7914d
description: Standardmäßig enthält die Datei "FormCode.cs" oder "FormCode.vb", die für ein mit InfoPath 2003 kompatibles Formularvorlagenprojekt erstellt wird, den gesamten Quellcode für die Programmierlogik des Formulars. Die Vorlage für das Projekt generiert eine Klasse in der Datei "FormCode.cs" oder "FormCode.vb", vergleichbar mit den Klassen in den folgenden Beispielen, in denen Sie Initialisierungs- und Bereinigungscode sowie Handler für Formularereignisse definieren können. Die Dateien "FormCode.cs" und "FormCode.vb" wenden ein System.ComponentModel.DescriptionAttribute-Attribut auf Assemblyebene an, das die Klasse als einzige Klasse identifiziert, in der Ereignishandler implementiert werden. Das InfoPathNamespace-Attribut (das vom InfoPathNamespaceAttribute-Typ implementiert wird) wird auf eine Klasse angewendet, um die in der Klasse verwendeten XML-DOM-Auswahl-Namespaces zu identifizieren. Die Namespaces, auf die in InfoPathNamespace verwiesen wird, werden vom InfoPath-Projektsystem verwaltet.
ms.openlocfilehash: 1ae81c261ad9927195c0a4ac6d80f58a16a6ebf1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299742"
---
# <a name="initialization-and-clean-up-code-using-infopath-2003-object-model"></a>Initialisierungs- und Bereinigungscode mit dem InfoPath 2003-Objektmodell

Standardmäßig enthält die Datei "FormCode.cs" oder "FormCode.vb", die für ein mit InfoPath 2003 kompatibles Formularvorlagenprojekt erstellt wird, den gesamten Quellcode für die Programmierlogik des Formulars. Die Vorlage für das Projekt generiert eine Klasse in der Datei "FormCode.cs" oder "FormCode.vb", vergleichbar mit den Klassen in den folgenden Beispielen, in denen Sie Initialisierungs- und Bereinigungscode sowie Handler für Formularereignisse definieren können. Die Dateien "FormCode.cs" und "FormCode.vb" wenden ein **System.ComponentModel.DescriptionAttribute**-Attribut auf Assemblyebene an, das die Klasse als einzige Klasse identifiziert, in der Ereignishandler implementiert werden. Das **INFOPATHNAMESPACE** -Attribut (das vom [InfoPathNamespaceAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathNamespaceAttribute.aspx) -Typ implementiert wird) wird auf eine Klasse angewendet, um die in der Klasse verwendeten XML-DOM-Auswahl-Namespaces zu identifizieren. Die Namespaces, auf die in **InfoPathNamespace** verwiesen wird, werden vom InfoPath-Projektsystem verwaltet. 
  
Die FormCode-Klasse selbst `_Startup` stellt `_Shutdown` Methoden bereit, die zum Ausführen von Initialisierungs-und Bereinigungsroutinen für alle Komponenten verwendet werden, die zusätzlich zu den standardmäßigen InfoPath-Funktionen erforderlich sind, während das Formular geöffnet ist. 
  
> [!IMPORTANT]
> Rufen Sie Member des InfoPath-Objektmodells nicht innerhalb der `_Startup` and- `_Shutdown` Methoden auf. Mit diesen Methoden sollten Sie nur Member externer Komponenten initialisieren und aufrufen. 
  
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
        "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-27-27'")]
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
        "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-29T22-36-40'")> _
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

Zusätzlich zur Bereitstellungeines Orts zum Schreiben von Initialisierungscode für zusätzliche Komponenten `_Startup` initialisiert die Methode `thisXDocument` die `thisApplication` und-Variablen, die in Ihrem Formularcode verwendet werden können, um auf die Member von [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) und Anwendung zuzugreifen. [ ](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx)Klassen im InfoPath-Objektmodell. Der für die Initialisierung der beiden Variablen erforderliche Code wird automatisch von der Projektvorlage generiert. 
  
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

Die folgenden Beispiele zeigen einen einfachen Ereignishandler für eine Schaltfläche, die `thisXDocument` die Variable für den Zugriff auf die [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) -Methode des [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) -Typs verwendet. 
  
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

Weitere Informationen zum Erstellen eines Ereignishandlers finden Sie unter [Hinzufügen eines Ereignishandlers mit dem InfoPath-Objektmodell 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
  
## <a name="the-shutdown-method"></a>_ShutDown (Methode)

Die `_Shutdown` Methode ist die letzte Methode, die aufgerufen wird, wenn ein Formular geschlossen wird. In dieser Methode können Sie beliebigen Code schreiben, der zum Bereinigen oder Fertigstellen von im Formular verwendeten Komponenten benötigt wird. 
  
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

Das folgende Beispiel zeigt, wie Sie eine Verbindung mit einer Microsoft SQL Server-Datenbank in `_Startup` der-Methode initialisieren und die Verbindung `_Shutdown` in der-Methode beenden. Damit dieses Beispiel ordnungsgemäß funktioniert, müssen Sie zuerst einen Verweis auf die System. Data-Assembly von .NET Framework festlegen, indem Sie im Menü **Projekt** auf **Verweis hinzufügen** klicken und dann die Komponente System. Data. dll auf **.net** auswählen. Registerkarte. Beachten Sie außerdem, `using System.Data.SqlClient` dass die `Imports System.Data.SqlClient)` (oder-Direktive oben in der Formular Codedatei hinzugefügt wurde, um Tastenkombinationen zu reduzieren. 
  
> [!NOTE]
> Benutzer eines InfoPath-Formulars mit Formularcode, der eine Verbindung mit einer SQL Server-Datenbank herstellt, benötigen möglicherweise Sicherheitsberechtigungen, abhängig von der Art der Bereitstellung des Formulars und der Definition der Sicherheitsrichtlinien. Weitere Informationen zur Sicherheit finden Sie unter Informationen zum [Sicherheitsmodell für Formularvorlagen mit Code](about-the-security-model-for-form-templates-with-code.md) und zum [Konfigurieren von Sicherheitseinstellungen für Formularvorlagen mit Code](how-to-configure-security-settings-for-form-templates-with-code.md). 
  
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
        "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-05T20-56-13'")]
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
            "xmlns:my='https://schemas.microsoft.com/office/infopath/2003/myXSD/2004-03-08T18-47-33'")>        _
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



[Hinzufügen eines Ereignishandlers mit dem InfoPath-Objektmodell 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

