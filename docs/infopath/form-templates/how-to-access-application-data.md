---
title: Zugreifen auf Anwendungsdaten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- application names [infopath 2007],accessing application name [InfoPath 2007],InfoPath 2007, accessing application data,accessing application version [InfoPath 2007],application versions [InfoPath 2007],language IDs [InfoPath 2007],LCID [InfoPath 2007],application data [InfoPath 2007],accessing language ID [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: Das InfoPath-Objektmodell mit verwaltetem Code stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Auf diese Daten wird über das Objekt der obersten Ebene in der InfoPath-Objektmodellhierarchie zugegriffen, das mithilfe der Application-Klasse instanziiert wird.
ms.openlocfilehash: 8a550e03f2a9da4a2897d79fa03739342416d3ca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631353"
---
# <a name="access-application-data"></a>Zugreifen auf Anwendungsdaten

Das InfoPath-Objektmodell mit verwaltetem Code stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Auf diese Daten wird über das Objekt der obersten Ebene in der InfoPath-Objektmodellhierarchie zugegriffen, das mithilfe der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) instanziiert wird. 
  
In einem InfoPath-Formularvorlagenprojekt mit verwaltetem Code, das mit Visual Studio 2012 erstellt wurde, können Sie **mithilfe** des Schlüsselworts C# oder Me (Visual Basic) auf eine Instanz der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) zugreifen, die die aktuelle InfoPath-Anwendung darstellt, die dann für den Zugriff auf die Eigenschaften und Methoden der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) verwendet werden kann.  
  
## <a name="example"></a>Beispiel

### <a name="displaying-the-application-name-version-and-language-id"></a>Anzeigen des Anwendungsnamens, der Version und der Sprachen-ID

Im folgenden Beispiel werden die Eigenschaften [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) und [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) verwendet, um den Namen und die Versionsnummer der ausgeführten Instanz von InfoPath zurückzugeben. Die [LanguageSettings-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) wird dann verwendet, um ein **LanguageSettings** -Objekt zurückzugeben, das wiederum verwendet wird, um die LCID (eine vierstellige Zahl) für die Sprache zurückzugeben, die derzeit für die InfoPath-Benutzeroberflächensprache verwendet wird. Schließlich werden alle diese Informationen in einem Meldungsfeld angezeigt. 
  
> [!IMPORTANT]
> Damit die **LanguageSettings-Eigenschaft** funktioniert, müssen Sie einen Verweis auf die Microsoft Office 14.0-Objektbibliothek über die **COM-Registerkarte** des Dialogfelds **"Verweis hinzufügen"** in Visual Studio 2012 einrichten. Dadurch wird ein Verweis auf den **Microsoft.Office.Core**-Namespace eingerichtet, der die **LanguageSettings**-Klasse enthält. Darüber hinaus muss das Formular als "Voll vertrauenswürdig" ausgeführt werden. 
  
Dieses Beispiel erfordert eine **using**- oder **Imports**-Direktive für den **Microsoft.Office.Core**-Namespace im Deklarationsabschnitt des Formularcodemoduls. 
  
```cs
string appName = this.Application.Name;
string appVersion = this.Application.Version;
LanguageSettings langSettings = 
   (LanguageSettings)this.Application.LanguageSettings;
int langID = 
   langSettings.get_LanguageID(MsoAppLanaguageID.msoLanguageIDUI);
MessageBox.Show(
   "Name: " + appName + System.Environment.NewLine +
   "Version: " + appVersion + System.Environment.NewLine +
   "Language ID: " + langID);
```

```vb
Dim appName As String appName = Me.Application.Name
Dim appVersion As String = Me.Application.Version
Dim langSettings As LanguageSettings = _
   DirectCast(Me.Application.LanguageSettings, LanguageSettings)
Dim langID As Integer = _
   langSettings.LanguageID(MsoAppLanaguageID.msoLanguageIDUI)
MessageBox.Show( _
   "Name: " + appName + System.Environment.NewLine + _
   "Version: " + appVersion + System.Environment.NewLine + _
   "Language ID: " + langID)
```


