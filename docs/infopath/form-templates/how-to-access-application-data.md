---
title: Zugreifen auf Anwendungsdaten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Anwendungsnamen [infopath 2007],Zugreifen auf anwendungsnamen [InfoPath 2007],InfoPath 2007, Zugreifen auf Anwendungsdaten,Zugreifen auf Anwendungsversion [InfoPath 2007],Anwendungsversionen [InfoPath 2007],Sprach-IDs [InfoPath 2007],LCID [InfoPath 2007],Anwendungsdaten [InfoPath 2007],Zugriff auf Sprach-ID [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: Das InfoPath-Objektmodell mit verwaltetem Code stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Auf diese Daten wird über das Objekt auf oberster Ebene in der InfoPath-Objektmodellhierarchie zugegriffen, das mithilfe der Application-Klasse instanziiert wird.
ms.openlocfilehash: 8da72313807584ee599d65701d009786dd631979
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417231"
---
# <a name="access-application-data"></a>Zugreifen auf Anwendungsdaten

Das InfoPath-Objektmodell mit verwaltetem Code stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Auf diese Daten wird über das Objekt auf oberster Ebene in der InfoPath-Objektmodellhierarchie zugegriffen, das mithilfe der [Application-Klasse instanziiert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) wird. 
  
In einem InfoPath-Formularvorlagenprojekt mit verwalteten Code, das mit Visual Studio  2012 erstellt wurde, können Sie das Schlüsselwort this (C#) oder **Me** (Visual Basic) verwenden, um auf eine Instanz der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) zu zugreifen, die die aktuelle InfoPath-Anwendung darstellt, die dann für den Zugriff auf die Eigenschaften und Methoden der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) verwendet werden kann. 
  
## <a name="example"></a>Beispiel

### <a name="displaying-the-application-name-version-and-language-id"></a>Anzeigen des Anwendungsnamens, der Version und der Sprachen-ID

Im folgenden Beispiel werden die [Eigenschaften Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) und [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) verwendet, um den Namen und die Versionsnummer der ausgeführten Instanz von InfoPath zurück zu geben. Die [LanguageSettings-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) wird dann zum Zurückgeben eines **LanguageSettings-Objekts** verwendet, das wiederum zum Zurückgeben der LCID (eine vierstellige Zahl) für die Sprache verwendet wird, die derzeit für die Benutzeroberflächensprache InfoPath verwendet wird. Schließlich werden alle diese Informationen in einem Meldungsfeld angezeigt. 
  
> [!IMPORTANT]
> Damit die **LanguageSettings-Eigenschaft** funktioniert, müssen Sie auf der Registerkarte **COM** des Dialogfelds Verweis hinzufügen  in Visual Studio 2012 einen Verweis auf die Microsoft Office 14.0-Objektbibliothek einrichten. Dadurch wird ein Verweis auf den **Microsoft.Office.Core**-Namespace eingerichtet, der die **LanguageSettings**-Klasse enthält. Darüber hinaus muss das Formular als "Voll vertrauenswürdig" ausgeführt werden. 
  
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


