---
title: Abschnitte des MapiSvc.inf-Dienstanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ea192ec6356cc3b929bf8379567144d3a54223f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405562"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="7be49-103">Abschnitte des MapiSvc.inf-Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="7be49-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="7be49-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7be49-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7be49-105">Mapisvc.inf enthält einen Dienstanbieterabschnitt für jeden der Einträge, die im Eintrag **Anbieter** im vorherigen Abschnitt "Nachrichtendienste" aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7be49-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="7be49-106">**Dienstanbieterabschnitte** ähneln Nachrichtendienstabschnitten, da beide Arten von Abschnitten Einträge in diesem Format enthalten:</span><span class="sxs-lookup"><span data-stu-id="7be49-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="7be49-107">**property-Tag** = Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7be49-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="7be49-108">Dienstanbieterabschnitte und Nachrichtendienstabschnitte unterscheiden sich jedoch darin, dass solche Eigenschaftseinträge der einzige Eintragstyp sind, der in Dienstanbieterabschnitten enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7be49-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="7be49-109">Es kann keine zusätzlichen oder verknüpften Abschnitte für Dienstanbieter sein. Alle Dienstanbieterinformationen müssen in dem einen Abschnitt enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="7be49-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="7be49-110">Einige der in Nachrichtendienstabschnitten festgelegten Eigenschaften werden auch in Abschnitten des Dienstanbieters festgelegt, da diese Eigenschaften für beides sinnvoll sind.</span><span class="sxs-lookup"><span data-stu-id="7be49-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="7be49-111">Die **PR_DISPLAY_NAME-Eigenschaft** ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="7be49-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="7be49-112">Sowohl Dienstanbieter als auch Nachrichtendienste haben einen Namen, der für die Anzeige auf der Benutzeroberfläche der Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7be49-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="7be49-113">Je nach Dienstanbieter ist dieser Name möglicherweise identisch.</span><span class="sxs-lookup"><span data-stu-id="7be49-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="7be49-114">Andere Eigenschaften sind spezifisch für Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="7be49-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="7be49-115">Typische Dienstanbieterabschnitte umfassen die folgenden Einträge, die alle erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="7be49-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="7be49-116">**PR_DISPLAY_NAME**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="7be49-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="7be49-117">**PR_PROVIDER_DISPLAY**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="7be49-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="7be49-118">**PR_PROVIDER_DLL_NAME**  =   _Name der DLL-Datei_</span><span class="sxs-lookup"><span data-stu-id="7be49-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="7be49-119">**PR_RESOURCE_TYPE**  =   _long_</span><span class="sxs-lookup"><span data-stu-id="7be49-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="7be49-120">**PR_RESOURCE_FLAGS**  =   _bitmask_</span><span class="sxs-lookup"><span data-stu-id="7be49-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="7be49-121">Der **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) ist ähnlich wie **PR_SERVICE_DLL_NAME**; Es gibt den Dateinamen für die DLL an, die den Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="7be49-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="7be49-122">Nachrichtendienstcode kann bei einem seiner Dienstanbieter in derselben DLL-Datei gespeichert werden oder als separate DLL vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7be49-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="7be49-123">Beachten Sie, dass unabhängig von der Zielplattform kein Suffix im Eintrag enthalten ist. MAPI übernimmt bei Bedarf das Hinzufügen eines Suffixes.</span><span class="sxs-lookup"><span data-stu-id="7be49-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="7be49-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) -Eintrag stellt den Typ des Dienstanbieters dar; Dienstanbieter legen sie auf die entsprechende vordefinierte Konstante fest.</span><span class="sxs-lookup"><span data-stu-id="7be49-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="7be49-125">Gültige Werte sind MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER und MAPI_AB_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="7be49-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="7be49-126">Ein weiterer Eigenschaftseintrag, der sowohl für Nachrichtendienste als auch für Dienstanbieter gilt, **gibt PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) -Eintrag Optionen an.</span><span class="sxs-lookup"><span data-stu-id="7be49-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="7be49-127">Die Einstellungen für diesen Eigenschaftseintrag können je nach Dienstanbieter variieren.</span><span class="sxs-lookup"><span data-stu-id="7be49-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="7be49-128">Einige Nachrichtenspeicheranbieter können z. B. PR_RESOURCE_FLAGS auf STATUS_NO_DEFAULT_STORE festlegen, wenn sie niemals als Standardnachrichtenspeicher verwendet werden können. </span><span class="sxs-lookup"><span data-stu-id="7be49-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="7be49-129">Es folgen drei Beispiele für Dienstanbieterabschnitte.</span><span class="sxs-lookup"><span data-stu-id="7be49-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="7be49-130">Der **Abschnitt [Ab-Anbieter]** ist der Abschnitt Dienstanbieter für den Standard-Adressbuchdienst.</span><span class="sxs-lookup"><span data-stu-id="7be49-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="7be49-131">Die **Abschnitte [MsgService Prov1]** und **[MsgService Prov2]** gehören zu My Own Service; Der erste Abschnitt ist ein Adressbuchanbieter, der zweite ein Abschnitt nachrichtenspeicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="7be49-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
```cpp
[AB Provider]
PR_DISPLAY_NAME=Default Address Book
PR_PROVIDER_DISPLAY=Default Address Book
PR_PROVIDER_DLL_NAME=AB.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
6600001e=C:\WINNT35\System32\DEFAB.TXT
[MsgService Prov1]
PR_DISPLAY_NAME=My Own Service
PR_PROVIDER_DISPLAY=My Own Address Book
PR_PROVIDER_DLL_NAME=MYXXX.DLL
PR_RESOURCE_TYPE=MAPI_AB_PROVIDER
[MsgService Prov2]
PR_DISPLAY_NAME=My Folders
PR_PROVIDER_DISPLAY=My Own Message Store
PR_RESOURCE_TYPE=MAPI_STORE_PROVIDER
PR_PROVIDER_DLL_NAME=MYZZZ.DLL
PR_RESOURCE_FLAGS=STATUS_NO_DEFAULT_STORE
66060003=00000000
66030003=00000000
34140102=78b2fa70aff711cd9bc800aa002fc45a
66090003=06000000
660A0003=03000000

```


