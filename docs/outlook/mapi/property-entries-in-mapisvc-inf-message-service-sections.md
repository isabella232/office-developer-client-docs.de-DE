---
title: Eigenschafteneinträge in den Nachrichtendienstabschnitten von MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 714f99e2-80fc-4785-b707-611d8a6c229f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 038c13d24f3d797f7a4f8f9b7692240ce8004b74
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580334"
---
# <a name="property-entries-in-mapisvcinf-message-service-sections"></a><span data-ttu-id="0c910-103">Eigenschafteneinträge in den Nachrichtendienstabschnitten von MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="0c910-103">Property Entries in MapiSvc.inf Message Service Sections</span></span>

  
  
<span data-ttu-id="0c910-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c910-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c910-105">Verwenden Sie dieses Format Einträge, die Eigenschaften festlegen:</span><span class="sxs-lookup"><span data-stu-id="0c910-105">Entries that set properties use this format:</span></span>
  
 <span data-ttu-id="0c910-106">**Eigenschafts-tag** **=** Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0c910-106">**property tag** **=** property value</span></span> 
  
<span data-ttu-id="0c910-107">Das Eigenschafts-Tag kann ein standard MAPI-Eigenschaftentag, wenn die Daten zur Konfiguration der Eigenschaften von MAPI vordefinierten darstellt, oder ein nicht standardmäßigen Tag sein, wenn die Daten keine MAPI-Eigenschaft darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c910-107">The property tag can be a standard MAPI property tag if the configuration data represents one of the properties predefined by MAPI, or a nonstandard tag if the data does not represent a MAPI property.</span></span> <span data-ttu-id="0c910-108">Das nicht standardmäßige Tag erfolgt durch den Wert für einen Eigenschaftenbezeichner mit einen Eigenschaftentyp kombinieren.</span><span class="sxs-lookup"><span data-stu-id="0c910-108">The nonstandard tag is made by combining the value for a property identifier with a property type.</span></span> <span data-ttu-id="0c910-109">Das Ergebnis ist eine hexadezimale Zahl 8 Ziffer.</span><span class="sxs-lookup"><span data-stu-id="0c910-109">The result is an 8 digit hexadecimal number.</span></span> <span data-ttu-id="0c910-110">Der Eigenschaftswert kann den Inhalt für das Eigenschafts-Tag sinnvoll sein.</span><span class="sxs-lookup"><span data-stu-id="0c910-110">The property value can be whatever makes sense for the property tag.</span></span> 
  
<span data-ttu-id="0c910-111">Nachricht Service Abschnitte können eine Reihe von Einträgen je nach den konfigurierten Dienst enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c910-111">Message service sections can contain a variety of entries depending on the message service being configured.</span></span> <span data-ttu-id="0c910-112">Die folgenden MAPI-Eigenschaften sind in der Regel in einer Nachricht im Abschnitt aufgelisteten Format enthalten:</span><span class="sxs-lookup"><span data-stu-id="0c910-112">The following MAPI properties are typically included in a message services section in the listed format:</span></span>
  
 <span data-ttu-id="0c910-113">**PR_DISPLAY_NAME** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="0c910-113">**PR_DISPLAY_NAME** =  _string_</span></span>
  
 <span data-ttu-id="0c910-114">**PR_SERVICE_DLL_NAME** =  _Name der DLL-Datei_</span><span class="sxs-lookup"><span data-stu-id="0c910-114">**PR_SERVICE_DLL_NAME** =  _name of DLL file_</span></span>
  
 <span data-ttu-id="0c910-115">**PR_SERVICE_ENTRY_NAME** =  _Name des Eintrags-Funktion_</span><span class="sxs-lookup"><span data-stu-id="0c910-115">**PR_SERVICE_ENTRY_NAME** =  _name of entry point function_</span></span>
  
 <span data-ttu-id="0c910-116">**PR_SERVICE_SUPPORT_FILES** =  _Liste der Dateien_</span><span class="sxs-lookup"><span data-stu-id="0c910-116">**PR_SERVICE_SUPPORT_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="0c910-117">**PR_SERVICE_DELETE_FILES** =  _Liste der Dateien_</span><span class="sxs-lookup"><span data-stu-id="0c910-117">**PR_SERVICE_DELETE_FILES** =  _list of files_</span></span>
  
 <span data-ttu-id="0c910-118">**PR_RESOURCE_FLAGS** =  _Bitmaske_</span><span class="sxs-lookup"><span data-stu-id="0c910-118">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="0c910-119">Die Zeichenfolge **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ist der Name des Diensts Nachricht, die in der Benutzeroberfläche, die den Namen angezeigt werden, der der Benutzer die Messagingdiensts zuordnet.</span><span class="sxs-lookup"><span data-stu-id="0c910-119">The **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) string is the name of the message service that is shown in the user interface, the name that the user associates with the message service.</span></span> <span data-ttu-id="0c910-120">Der Anzeigename ist ein optionaler Eintrag in mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="0c910-120">The display name is an optional entry in mapisvc.inf.</span></span> <span data-ttu-id="0c910-121">In einigen Fällen wird der Anzeigename aus zwei Teilen bestehen; eine durch den Dienst zugewiesen und einen Teil durch den Benutzer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="0c910-121">Sometimes the display name will be made up of two parts; a part assigned by the message service and a part assigned by the user.</span></span> <span data-ttu-id="0c910-122">Wenn der Benutzer für das Zuweisen einer der Teile zuständig ist, erfolgt dies in der Regel mit einem speziellen Dialogfenster bekannt als einem Eigenschaftenfenster bereitgestellt, die vom Nachrichtendienst von einer Clientanwendung aus gesteuert.</span><span class="sxs-lookup"><span data-stu-id="0c910-122">If the user is responsible for assigning one of the parts, this is typically handled with a special dialog box known as a property sheet supplied by the message service under the control of a client application.</span></span> 
  
<span data-ttu-id="0c910-123">Die enthaltenen Informationen für den Eintrag **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) ist der Name der DLL, die den Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="0c910-123">The information provided for the **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) entry is the name of the DLL that contains the message service.</span></span> <span data-ttu-id="0c910-124">Die enthaltenen Informationen für den Eintrag **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) ist der Name der Funktion Eintrag Punkt innerhalb dieser DLL, die MAPI-so konfigurieren Sie den Dienst aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0c910-124">The information provided for the **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) entry is the name of the entry point function within that DLL that MAPI calls to configure the message service.</span></span> 
  
<span data-ttu-id="0c910-125">Die Dateien in den Eintrag **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) sind Dateien, die mit dem Nachrichtendienst installiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0c910-125">The files listed in the **PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md)) entry are files that must be installed with the message service.</span></span> <span data-ttu-id="0c910-126">Die Dateien in den Eintrag **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) müssen ebenso entfernt werden, wenn der Nachrichtendienst entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="0c910-126">Likewise, the files in the **PR_SERVICE_DELETE_FILES** ([PidTagServiceDeleteFiles](pidtagservicedeletefiles-canonical-property.md)) entry must be removed when the message service is removed.</span></span> 
  
<span data-ttu-id="0c910-127">Der Eintrag **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) ist eine Auflistung von Optionen für den Dienst definiert.</span><span class="sxs-lookup"><span data-stu-id="0c910-127">The **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry is a collection of options defined for the message service.</span></span> <span data-ttu-id="0c910-128">Beispielsweise wird das Bit SERVICE_SINGLE_COPY festgelegt, wenn der Nachrichtendienst nur einmal in einem bestimmten Profil angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="0c910-128">For example, the SERVICE_SINGLE_COPY bit is set when the message service can only appear once in a given profile.</span></span> <span data-ttu-id="0c910-129">Das SERVICE_NO_PRIMARY_IDENTITY Bit ist festgelegt, wenn der Nachrichtendienst nicht Identitätsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0c910-129">The SERVICE_NO_PRIMARY_IDENTITY bit is set if the message service does not provide identity information.</span></span> 
  
<span data-ttu-id="0c910-130">Führen Sie die beiden Beispiele für nicht standardmäßigen Eigenschafteneinträge.</span><span class="sxs-lookup"><span data-stu-id="0c910-130">Two examples of nonstandard property entries follow.</span></span> <span data-ttu-id="0c910-131">Der erste Eintrag gibt den Pfad zu der Datei durch das Standard-Adressbuch als Wert der Eigenschaft verwendet. der zweite Eintrag gibt den Eigenschaftswert einer numerischen.</span><span class="sxs-lookup"><span data-stu-id="0c910-131">The first entry specifies the path to the file used by the Default Address Book as the property value; the second entry specifies a numeric property value.</span></span> <span data-ttu-id="0c910-132">Beide Einträge haben Bedeutung, die speziell für den Dienst AB.</span><span class="sxs-lookup"><span data-stu-id="0c910-132">Both entries have meaning specific to the AB message service.</span></span>
  
```cpp
6600001e=full path to file
66040003=integer

```


