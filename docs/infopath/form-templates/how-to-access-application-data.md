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
# <a name="access-application-data"></a><span data-ttu-id="5807a-105">Zugreifen auf Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="5807a-105">Access Application Data</span></span>

<span data-ttu-id="5807a-106">Das InfoPath-Objektmodell mit verwaltetem Code stellt Objekte und Auflistungen bereit, mit deren Hilfe der Zugriff auf Informationen zur InfoPath-Anwendung ermöglicht wird, einschließlich Informationen zu dem einem Formular zugrunde liegenden XML-Dokument und der Formulardefinitionsdatei (XSF).</span><span class="sxs-lookup"><span data-stu-id="5807a-106">The InfoPath managed code object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file.</span></span> <span data-ttu-id="5807a-107">Auf diese Daten wird über das Objekt auf oberster Ebene in der InfoPath-Objektmodellhierarchie zugegriffen, das mithilfe der [Application-Klasse instanziiert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) wird.</span><span class="sxs-lookup"><span data-stu-id="5807a-107">This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
<span data-ttu-id="5807a-108">In einem InfoPath-Formularvorlagenprojekt mit verwalteten Code, das mit Visual Studio  2012 erstellt wurde, können Sie das Schlüsselwort this (C#) oder **Me** (Visual Basic) verwenden, um auf eine Instanz der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) zu zugreifen, die die aktuelle InfoPath-Anwendung darstellt, die dann für den Zugriff auf die Eigenschaften und Methoden der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5807a-108">In an InfoPath managed code form template project created using Visual Studio 2012, you can use the **this** (C#) or **Me** (Visual Basic) keyword to access an instance of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class that represents the current InfoPath application, which can then be used to access the properties and methods of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class.</span></span> 
  
## <a name="example"></a><span data-ttu-id="5807a-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5807a-109">Example</span></span>

### <a name="displaying-the-application-name-version-and-language-id"></a><span data-ttu-id="5807a-110">Anzeigen des Anwendungsnamens, der Version und der Sprachen-ID</span><span class="sxs-lookup"><span data-stu-id="5807a-110">Displaying the Application Name, Version, and Language ID</span></span>

<span data-ttu-id="5807a-111">Im folgenden Beispiel werden die [Eigenschaften Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) und [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) der [Application-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) verwendet, um den Namen und die Versionsnummer der ausgeführten Instanz von InfoPath zurück zu geben.</span><span class="sxs-lookup"><span data-stu-id="5807a-111">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class are used to return the name and version number of the running instance of InfoPath.</span></span> <span data-ttu-id="5807a-112">Die [LanguageSettings-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) wird dann zum Zurückgeben eines **LanguageSettings-Objekts** verwendet, das wiederum zum Zurückgeben der LCID (eine vierstellige Zahl) für die Sprache verwendet wird, die derzeit für die Benutzeroberflächensprache InfoPath verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5807a-112">The [LanguageSettings](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.LanguageSettings.aspx) property is then used to return a **LanguageSettings** object, which in turn is used to return the LCID (a four-digit number) for the language that is currently being used for the InfoPath user interface language.</span></span> <span data-ttu-id="5807a-113">Schließlich werden alle diese Informationen in einem Meldungsfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5807a-113">Finally, all of this information is displayed in a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5807a-114">Damit die **LanguageSettings-Eigenschaft** funktioniert, müssen Sie auf der Registerkarte **COM** des Dialogfelds Verweis hinzufügen  in Visual Studio 2012 einen Verweis auf die Microsoft Office 14.0-Objektbibliothek einrichten.</span><span class="sxs-lookup"><span data-stu-id="5807a-114">For the **LanguageSettings** property to work, you must establish a reference to the Microsoft Office 14.0 Object Library from the **COM** tab of the **Add Reference** dialog box in Visual Studio 2012.</span></span> <span data-ttu-id="5807a-115">Dadurch wird ein Verweis auf den **Microsoft.Office.Core**-Namespace eingerichtet, der die **LanguageSettings**-Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="5807a-115">This will establish a reference to the **Microsoft.Office.Core** namespace, which contains the **LanguageSettings** class.</span></span> <span data-ttu-id="5807a-116">Darüber hinaus muss das Formular als "Voll vertrauenswürdig" ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5807a-116">Additionally, the form must be running as Full Trust.</span></span> 
  
<span data-ttu-id="5807a-117">Dieses Beispiel erfordert eine **using**- oder **Imports**-Direktive für den **Microsoft.Office.Core**-Namespace im Deklarationsabschnitt des Formularcodemoduls.</span><span class="sxs-lookup"><span data-stu-id="5807a-117">This example requires a **using** or **Imports** directive for the **Microsoft.Office.Core** namespace in the declarations section of the form code module.</span></span> 
  
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


