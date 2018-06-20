---
title: Access-Anwendungsdaten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Anwendungsnamen [Infopath 2007], zugreifen auf Anwendungsnamen [InfoPath 2007], InfoPath 2007, zugreifen auf Anwendungsdaten, zugreifen auf Anwendungsversion [InfoPath 2007], Anwendungsversionen [InfoPath 2007], Sprach-IDs [InfoPath 2007], [InfoPath LCID 2007] Anwendungsdaten [InfoPath 2007], den Zugriff auf die Sprachen-ID [InfoPath 2007]
localization_priority: Normal
ms.assetid: 2698d059-9955-4eec-85a6-79defb64e07e
description: Die InfoPath-Objektmodell für verwalteten Code bietet Objekte und Auflistungen, die verwendet werden können, um Zugriff auf Informationen über die InfoPath-Anwendung, einschließlich Informationen in Bezug auf einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Der Zugriff auf diese Daten erfolgt über das Objekt der obersten Ebene in der Hierarchie InfoPath-Objektmodells, die mithilfe der Application-Klasse instanziiert wird.
ms.openlocfilehash: 3c3f6be4e90e292eb572da836bca0a8dcf1883cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790722"
---
# <a name="access-application-data"></a>Access-Anwendungsdaten

Die InfoPath-Objektmodell für verwalteten Code bietet Objekte und Auflistungen, die verwendet werden können, um Zugriff auf Informationen über die InfoPath-Anwendung, einschließlich Informationen in Bezug auf einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF). Der Zugriff auf diese Daten erfolgt über das Objekt der obersten Ebene in der Hierarchie InfoPath-Objektmodells, die mithilfe der [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse instanziiert wird. 
  
In einer InfoPath verwaltetem Code Formularvorlagenprojekt mit Visual Studio 2012 erstellt können Sie das **dieser** (c#) oder Schlüsselwort **Me** (Visual Basic) verwenden, um eine Instanz der Klasse [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) zuzugreifen, die aktuelle InfoPath-Anwendung darstellt, die kann dann Zugriff auf die Eigenschaften und Methoden des [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse verwendet werden. 
  
## <a name="example"></a>Beispiel

### <a name="displaying-the-application-name-version-and-language-id"></a>Anzeigen des Anwendungsnamens, der Version und der Sprachen-ID

Im folgenden Beispiel werden die Eigenschaften [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) und [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) des [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse zum Zurückgeben der Anzahl Name und Version der ausgeführten Instanz von InfoPath verwendet. Die [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) -Eigenschaft wird verwendet, die ein **LanguageSettings** -Objekt zurückzugeben, das wiederum verwendet wird, um die LCID (eine vierstellige Zahl) zurückzugeben für die Sprache, die derzeit für die Sprache der Benutzeroberfläche InfoPath verwendet wird. Alle diese Informationen wird dann angezeigt in einem Meldungsfeld. 
  
> [!IMPORTANT]
> Für die **LanguageSettings** -Eigenschaft funktioniert müssen Sie einen Verweis auf die Microsoft Office 14.0-Objektbibliothek auf der Registerkarte **COM** im Dialogfeld **Verweis hinzufügen** in Visual Studio 2012 einrichten. Dadurch wird einen Verweis auf den **Microsoft.Office.Core** -Namespace hergestellt, die die **LanguageSettings** -Klasse enthält. Darüber hinaus muss das Formular als voll vertrauenswürdig ausgeführt werden. 
  
Dieses Beispiel erfordert eine **Using-** oder **Imports** -Direktive für den **Microsoft.Office.Core** -Namespace im Deklarationsabschnitt des formularcodemoduls. 
  
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


