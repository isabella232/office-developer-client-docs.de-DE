---
title: Eigenschafts Einträge in den Nachrichtendienst Abschnitten von MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328518"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="ff82b-103">Eigenschafts Einträge in den Nachrichtendienst Abschnitten von MapiSvc. inf</span><span class="sxs-lookup"><span data-stu-id="ff82b-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="ff82b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff82b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff82b-105">Einträge, die Eigenschaften festlegen, verwenden dieses Format:</span><span class="sxs-lookup"><span data-stu-id="ff82b-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="ff82b-106">**Property-Tag** **=** Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ff82b-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="ff82b-107">Bei dem Property-Tag kann es sich um ein Standardmäßiges MAPI-Eigenschafts handeln, wenn die Konfigurationsdaten eine der von MAPI vordefinierten Eigenschaften darstellen, oder ein nicht standardmäßiges Tag, wenn die Daten keine MAPI-Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="ff82b-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="ff82b-108">Das Nonstandard-Tag wird durch Kombinieren des Werts für einen Eigenschaftenbezeichner mit einem Eigenschaftentyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="ff82b-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="ff82b-109">Das Ergebnis ist eine achtstellige Hexadezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="ff82b-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="ff82b-110">Der Eigenschaftswert kann für das Property-Tag sinnvoll sein.</span><span class="sxs-lookup"><span data-stu-id="ff82b-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="ff82b-111">Nachrichtendienst Abschnitte können eine Vielzahl von Einträgen in Abhängigkeit vom konfigurierten Nachrichtendienst enthalten.</span><span class="sxs-lookup"><span data-stu-id="ff82b-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="ff82b-112">Die folgenden MAPI-Eigenschaften sind in der Regel in einem Abschnitt für Nachrichtendienste im aufgeführten Format enthalten:</span><span class="sxs-lookup"><span data-stu-id="ff82b-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="ff82b-113">**PR_DISPLAY_NAME** =  -_Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="ff82b-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="ff82b-114">**PR_SERVICE_DLL_NAME** =  _Name der DLL-Datei_</span><span class="sxs-lookup"><span data-stu-id="ff82b-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="ff82b-115">**PR_SERVICE_ENTRY_NAME** =  _Name der Einstiegspunktfunktion_</span><span class="sxs-lookup"><span data-stu-id="ff82b-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="ff82b-116">**PR_SERVICE_SUPPORT_FILES** =  _-Liste der Dateien_</span><span class="sxs-lookup"><span data-stu-id="ff82b-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="ff82b-117">**PR_SERVICE_DELETE_FILES** =  _-Liste der Dateien_</span><span class="sxs-lookup"><span data-stu-id="ff82b-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="ff82b-118">**PR_RESOURCE_FLAGS** =  __ -Bitmaske</span><span class="sxs-lookup"><span data-stu-id="ff82b-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="ff82b-119">Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Zeichenfolge ist der Name des Nachrichtendiensts, der auf der Benutzeroberfläche angezeigt wird, der Name, den der Benutzer dem Nachrichtendienst zuordnet.</span><span class="sxs-lookup"><span data-stu-id="ff82b-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="ff82b-120">Der Anzeigename ist ein optionaler Eintrag in MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="ff82b-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="ff82b-121">Manchmal besteht der Anzeigename aus zwei Teilen; ein vom Nachrichtendienst zugewiesenes Teil und ein vom Benutzer zugewiesenes Teil.</span><span class="sxs-lookup"><span data-stu-id="ff82b-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="ff82b-122">Wenn der Benutzer für die Zuweisung eines der Teile verantwortlich ist, wird dies in der Regel mit einem speziellen Dialogfeld behandelt, das als Eigenschaftenblatt bezeichnet wird, das vom Nachrichtendienst unter der Steuerung einer Clientanwendung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ff82b-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="ff82b-123">Die für den **PR_SERVICE_DLL_NAME** ([pidtagservicedllname (](pidtagservicedllname-canonical-property.md)) bereitgestellten Informationen sind der Name der dll, die den Nachrichtendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="ff82b-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="ff82b-124">Die Informationen für den **PR_SERVICE_ENTRY_NAME** ([pidtagserviceentryname (](pidtagserviceentryname-canonical-property.md)) sind der Name der Einstiegspunktfunktion innerhalb der dll, die MAPI zum Konfigurieren des Nachrichtendiensts aufruft.</span><span class="sxs-lookup"><span data-stu-id="ff82b-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="ff82b-125">Bei den im **PR_SERVICE_SUPPORT_FILES** ([pidtagservicesupportfiles (](pidtagservicesupportfiles-canonical-property.md)) aufgeführten Dateien handelt es sich um Dateien, die mit dem Nachrichtendienst installiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ff82b-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="ff82b-126">Entsprechend müssen die Dateien im **PR_SERVICE_DELETE_FILES** ([pidtagservicedeletefiles (](pidtagservicedeletefiles-canonical-property.md))-Eintrag entfernt werden, wenn der Nachrichtendienst entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ff82b-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="ff82b-127">Der **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eintrag ist eine Sammlung von Optionen, die für den Nachrichtendienst definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ff82b-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="ff82b-128">Beispielsweise wird das SERVICE_SINGLE_COPY-Bit festgelegt, wenn der Nachrichtendienst nur einmal in einem bestimmten Profil angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ff82b-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="ff82b-129">Das SERVICE_NO_PRIMARY_IDENTITY-Bit wird festgelegt, wenn der Nachrichtendienst keine Identitätsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ff82b-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="ff82b-130">Es folgen zwei Beispiele für nicht standardmäßige Eigenschafts Einträge.</span><span class="sxs-lookup"><span data-stu-id="ff82b-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="ff82b-131">Der erste Eintrag gibt den Pfad zu der Datei an, die vom Standardadressbuch als Eigenschaftswert verwendet wird. der zweite Eintrag gibt einen numerischen Eigenschaftswert an.</span><span class="sxs-lookup"><span data-stu-id="ff82b-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="ff82b-132">Beide Einträge haben eine bestimmte Bedeutung für den AB-Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="ff82b-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


