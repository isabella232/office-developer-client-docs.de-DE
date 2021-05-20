---
title: Eigenschaftseinträge in MapiSvc.inf-Nachrichtendienstabschnitten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ad2732f2f8dba4f506318a1b6faefb617a60584a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427997"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="24047-103">Eigenschaftseinträge in MapiSvc.inf-Nachrichtendienstabschnitten</span><span class="sxs-lookup"><span data-stu-id="24047-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="24047-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24047-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24047-105">Einträge, die Eigenschaften festlegen, verwenden dieses Format:</span><span class="sxs-lookup"><span data-stu-id="24047-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="24047-106">**Property-Tag** **=** Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="24047-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="24047-107">Das Eigenschaftstag kann ein standardmäßiges MAPI-Eigenschaftstag sein, wenn die Konfigurationsdaten eine der von MAPI vordefinierten Eigenschaften oder ein nicht standardmäßiges Tag darstellen, wenn die Daten keine MAPI-Eigenschaft darstellen.</span><span class="sxs-lookup"><span data-stu-id="24047-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="24047-108">Das nicht standardmäßige Tag wird durch Kombinieren des Werts für einen Eigenschaftenbezeichner mit einem Eigenschaftentyp hergestellt.</span><span class="sxs-lookup"><span data-stu-id="24047-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="24047-109">Das Ergebnis ist eine 8-stellige Hexadezimalzahl.</span><span class="sxs-lookup"><span data-stu-id="24047-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="24047-110">Der Eigenschaftswert kann für das Eigenschaftstag sinnvoll sein.</span><span class="sxs-lookup"><span data-stu-id="24047-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="24047-111">Nachrichtendienstabschnitte können je nach konfigurierten Nachrichtendienst eine Vielzahl von Einträgen enthalten.</span><span class="sxs-lookup"><span data-stu-id="24047-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="24047-112">Die folgenden MAPI-Eigenschaften sind in der Regel in einem Nachrichtendienstabschnitt im aufgeführten Format enthalten:</span><span class="sxs-lookup"><span data-stu-id="24047-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="24047-113">**PR_DISPLAY_NAME**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="24047-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="24047-114">**PR_SERVICE_DLL_NAME**  =   _Name der DLL-Datei_</span><span class="sxs-lookup"><span data-stu-id="24047-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="24047-115">**PR_SERVICE_ENTRY_NAME**  =   _Name der Einstiegspunktfunktion_</span><span class="sxs-lookup"><span data-stu-id="24047-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="24047-116">**PR_SERVICE_SUPPORT_FILES**  =   _Liste der Dateien_</span><span class="sxs-lookup"><span data-stu-id="24047-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="24047-117">**PR_SERVICE_DELETE_FILES**  =   _Liste der Dateien_</span><span class="sxs-lookup"><span data-stu-id="24047-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="24047-118">**PR_RESOURCE_FLAGS**  =   _bitmask_</span><span class="sxs-lookup"><span data-stu-id="24047-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="24047-119">Die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Zeichenfolge ist der Name des Nachrichtendiensts, der auf der Benutzeroberfläche angezeigt wird, der Name, den der Benutzer dem Nachrichtendienst zuzeigt.</span><span class="sxs-lookup"><span data-stu-id="24047-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="24047-120">Der Anzeigename ist ein optionaler Eintrag in mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="24047-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="24047-121">Manchmal besteht der Anzeigename aus zwei Teilen. ein vom Nachrichtendienst zugewiesener Teil und ein vom Benutzer zugewiesener Teil.</span><span class="sxs-lookup"><span data-stu-id="24047-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="24047-122">Wenn der Benutzer für die Zuweisung eines der Teile verantwortlich ist, wird dies in der Regel mit einem speziellen Dialogfeld behandelt, das als Eigenschaftenblatt bezeichnet wird, das vom Nachrichtendienst unter der Kontrolle einer Clientanwendung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="24047-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="24047-123">Die Für den Eintrag PR_SERVICE_DLL_NAME **(** [PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) bereitgestellten Informationen ist der Name der DLL, die den Nachrichtendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="24047-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="24047-124">Die informationen für den **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) -Eintrag ist der Name der Einstiegspunktfunktion innerhalb dieser DLL, die MAPI aufruft, um den Nachrichtendienst zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="24047-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="24047-125">Die im Eintrag PR_SERVICE_SUPPORT_FILES **(** [PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) aufgeführten Dateien sind Dateien, die mit dem Nachrichtendienst installiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="24047-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="24047-126">Ebenso müssen die Dateien im **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entfernt werden, wenn der Nachrichtendienst entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="24047-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="24047-127">Der **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ist eine Auflistung von Optionen, die für den Nachrichtendienst definiert sind.</span><span class="sxs-lookup"><span data-stu-id="24047-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="24047-128">Beispielsweise wird das SERVICE_SINGLE_COPY festgelegt, wenn der Nachrichtendienst nur einmal in einem bestimmten Profil angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="24047-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="24047-129">Das SERVICE_NO_PRIMARY_IDENTITY bit wird festgelegt, wenn der Nachrichtendienst keine Identitätsinformationen zur Verfügung stellt.</span><span class="sxs-lookup"><span data-stu-id="24047-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="24047-130">Es folgen zwei Beispiele für nicht standardmäßige Eigenschaftseinträge.</span><span class="sxs-lookup"><span data-stu-id="24047-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="24047-131">Der erste Eintrag gibt den Pfad zu der Datei an, die vom Standardadressenbuch als Eigenschaftswert verwendet wird. Der zweite Eintrag gibt einen numerischen Eigenschaftswert an.</span><span class="sxs-lookup"><span data-stu-id="24047-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="24047-132">Beide Einträge haben eine bedeutungsspezifische Bedeutung für den Ab-Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="24047-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


