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
# <a name="access-application-data"></a><span data-ttu-id="aaf22-105">Access-Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="aaf22-105">Access Application Data</span></span>

<span data-ttu-id="aaf22-106">Die InfoPath-Objektmodell für verwalteten Code bietet Objekte und Auflistungen, die verwendet werden können, um Zugriff auf Informationen über die InfoPath-Anwendung, einschließlich Informationen in Bezug auf einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF).</span><span class="sxs-lookup"><span data-stu-id="aaf22-106">The InfoPath managed code object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file.</span></span> <span data-ttu-id="aaf22-107">Der Zugriff auf diese Daten erfolgt über das Objekt der obersten Ebene in der Hierarchie InfoPath-Objektmodells, die mithilfe der [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse instanziiert wird.</span><span class="sxs-lookup"><span data-stu-id="aaf22-107">This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
<span data-ttu-id="aaf22-108">In einer InfoPath verwaltetem Code Formularvorlagenprojekt mit Visual Studio 2012 erstellt können Sie das **dieser** (c#) oder Schlüsselwort **Me** (Visual Basic) verwenden, um eine Instanz der Klasse [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) zuzugreifen, die aktuelle InfoPath-Anwendung darstellt, die kann dann Zugriff auf die Eigenschaften und Methoden des [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="aaf22-108">In an InfoPath managed code form template project created using Visual Studio 2012, you can use the **this** (C#) or **Me** (Visual Basic) keyword to access an instance of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that represents the current InfoPath application, which can then be used to access the properties and methods of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
## <a name="example"></a><span data-ttu-id="aaf22-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="aaf22-109">Example</span></span>

### <a name="displaying-the-application-name-version-and-language-id"></a><span data-ttu-id="aaf22-110">Anzeigen des Anwendungsnamens, der Version und der Sprachen-ID</span><span class="sxs-lookup"><span data-stu-id="aaf22-110">Displaying the Application Name, Version, and Language ID</span></span>

<span data-ttu-id="aaf22-111">Im folgenden Beispiel werden die Eigenschaften [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) und [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) des [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) -Klasse zum Zurückgeben der Anzahl Name und Version der ausgeführten Instanz von InfoPath verwendet.</span><span class="sxs-lookup"><span data-stu-id="aaf22-111">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class are used to return the name and version number of the running instance of InfoPath.</span></span> <span data-ttu-id="aaf22-112">Die [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) -Eigenschaft wird verwendet, die ein **LanguageSettings** -Objekt zurückzugeben, das wiederum verwendet wird, um die LCID (eine vierstellige Zahl) zurückzugeben für die Sprache, die derzeit für die Sprache der Benutzeroberfläche InfoPath verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aaf22-112">The [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) property is then used to return a **LanguageSettings** object, which in turn is used to return the LCID (a four-digit number) for the language that is currently being used for the InfoPath user interface language.</span></span> <span data-ttu-id="aaf22-113">Alle diese Informationen wird dann angezeigt in einem Meldungsfeld.</span><span class="sxs-lookup"><span data-stu-id="aaf22-113">Finally, all of this information is displayed in a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="aaf22-114">Für die **LanguageSettings** -Eigenschaft funktioniert müssen Sie einen Verweis auf die Microsoft Office 14.0-Objektbibliothek auf der Registerkarte **COM** im Dialogfeld **Verweis hinzufügen** in Visual Studio 2012 einrichten.</span><span class="sxs-lookup"><span data-stu-id="aaf22-114">For the **LanguageSettings** property to work, you must establish a reference to the Microsoft Office 14.0 Object Library from the **COM** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> <span data-ttu-id="aaf22-115">Dadurch wird einen Verweis auf den **Microsoft.Office.Core** -Namespace hergestellt, die die **LanguageSettings** -Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="aaf22-115">This will establish a reference to the **Microsoft.Office.Core** namespace, which contains the **LanguageSettings** class.</span></span> <span data-ttu-id="aaf22-116">Darüber hinaus muss das Formular als voll vertrauenswürdig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="aaf22-116">Additionally, the form must be running as Full Trust.</span></span> 
  
<span data-ttu-id="aaf22-117">Dieses Beispiel erfordert eine **Using-** oder **Imports** -Direktive für den **Microsoft.Office.Core** -Namespace im Deklarationsabschnitt des formularcodemoduls.</span><span class="sxs-lookup"><span data-stu-id="aaf22-117">This example requires a **using** or **Imports** directive for the **Microsoft.Office.Core** namespace in the declarations section of the form code module.</span></span> 
  
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


