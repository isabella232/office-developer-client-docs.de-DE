---
title: Dienstanbieterabschnitte in MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ab17dcf2-409b-4a57-9cc4-5794f995cd3e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 05666d8d6b7279588b4b442151640fa1696aedda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586781"
---
# <a name="mapisvcinf-service-provider-sections"></a><span data-ttu-id="c2a88-103">Dienstanbieterabschnitte in MapiSvc.inf</span><span class="sxs-lookup"><span data-stu-id="c2a88-103">MapiSvc.inf Service Provider Sections</span></span>

<span data-ttu-id="c2a88-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2a88-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2a88-105">MAPISVC.inf enthält einen Dienst Anbieterabschnitt für jeden der Einträge in der **Anbieter** -Eintrag im vorherigen Abschnitt der Nachricht Dienste aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2a88-105">Mapisvc.inf includes one service provider section for each of the entries listed in the **Providers** entry in the preceding message services section.</span></span> <span data-ttu-id="c2a88-106">**Service** Provider Abschnitte ähneln Nachricht Service Abschnitte, dass beide Arten von Abschnitten Einträge in diesem Format enthalten:</span><span class="sxs-lookup"><span data-stu-id="c2a88-106">**Service** provider sections are similar to message service sections in that both types of sections contain entries in this format:</span></span> 
  
<span data-ttu-id="c2a88-107">**Eigenschafts-Tag** = Wert-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c2a88-107">**property tag** = property value</span></span> 
  
<span data-ttu-id="c2a88-108">Unterscheiden sich jedoch Service Provider Abschnitte und Nachricht Service Abschnitte, solche Eigenschafteneinträge die einzige Art des Eintrags im Service Provider Abschnitte enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="c2a88-108">However, service provider sections and message service sections differ in that such property entries are the only type of entry included in service provider sections.</span></span> <span data-ttu-id="c2a88-109">Es kann keine zusätzliche oder verknüpfte Abschnitte für Dienstanbieter vorhanden sein. alle Informationen muss in einem Abschnitt enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="c2a88-109">There can be no additional or linked sections for service providers; all service provider information must be contained within the one section.</span></span> 
  
<span data-ttu-id="c2a88-110">Einige der Eigenschaften in Nachricht Service Abschnitten festgelegt werden auch in Service Provider Abschnitten festgelegt, da diese Eigenschaften für beide sinnvoll.</span><span class="sxs-lookup"><span data-stu-id="c2a88-110">Some of the properties set in message service sections are also set in service provider sections because these properties make sense for both.</span></span> <span data-ttu-id="c2a88-111">Die **PR_DISPLAY_NAME** -Eigenschaft ist ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="c2a88-111">The **PR_DISPLAY_NAME** property is an example.</span></span> <span data-ttu-id="c2a88-112">Dienstanbieter und Message-Dienste haben einen Namen, der für die Anzeige in der Benutzeroberfläche für die Konfiguration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c2a88-112">Both service providers and message services have a name that is used for display in the configuration user interface.</span></span> <span data-ttu-id="c2a88-113">Je nach den Dienstanbieter diesem Namen oder möglicherweise nicht identisch.</span><span class="sxs-lookup"><span data-stu-id="c2a88-113">Depending on the service provider, that name may or may not be the same.</span></span> <span data-ttu-id="c2a88-114">Andere Eigenschaften sind spezifisch für den Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="c2a88-114">Other properties are specific to service providers.</span></span> 
  
<span data-ttu-id="c2a88-115">Normalen Service Provider Abschnitte enthalten die folgenden Einträge, die alle erforderlich sind:</span><span class="sxs-lookup"><span data-stu-id="c2a88-115">Typical service provider sections include the following entries, all of which are required:</span></span>
  
<span data-ttu-id="c2a88-116">**PR_DISPLAY_NAME** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="c2a88-116">**PR_DISPLAY_NAME** =  _string_</span></span>
  
<span data-ttu-id="c2a88-117">**PR_PROVIDER_DISPLAY** =  _Zeichenfolge_</span><span class="sxs-lookup"><span data-stu-id="c2a88-117">**PR_PROVIDER_DISPLAY** =  _string_</span></span>
  
<span data-ttu-id="c2a88-118">**PR_PROVIDER_DLL_NAME** =  _Name der DLL-Datei_</span><span class="sxs-lookup"><span data-stu-id="c2a88-118">**PR_PROVIDER_DLL_NAME** =  _name of DLL file_</span></span>
  
<span data-ttu-id="c2a88-119">**PR_RESOURCE_TYPE** =  _lang_</span><span class="sxs-lookup"><span data-stu-id="c2a88-119">**PR_RESOURCE_TYPE** =  _long_</span></span>
  
<span data-ttu-id="c2a88-120">**PR_RESOURCE_FLAGS** =  _Bitmaske_</span><span class="sxs-lookup"><span data-stu-id="c2a88-120">**PR_RESOURCE_FLAGS** =  _bitmask_</span></span>
  
<span data-ttu-id="c2a88-121">**PR_SERVICE_DLL_NAME**entspricht der Eintrag **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) ist. Es gibt den Dateinamen für die DLL, die den Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="c2a88-121">The **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) entry is similar to **PR_SERVICE_DLL_NAME**; it indicates the filename for the DLL that contains the service provider.</span></span> <span data-ttu-id="c2a88-122">Message Authentication Servicecode mit einem der der Dienstanbieter in der gleichen DLL-Datei gespeichert werden kann oder als eine separate DLL vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c2a88-122">Message service code may be stored with one of its service providers in the same DLL file or exist as a separate DLL.</span></span> <span data-ttu-id="c2a88-123">Beachten Sie, dass kein Suffix in den Eintrag unabhängig von der Zielplattform enthalten ist. MAPI kümmert ein Suffix hinzufügen, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c2a88-123">Note that no suffix is included in the entry regardless of the target platform; MAPI takes care of adding a suffix if necessary.</span></span> 
  
<span data-ttu-id="c2a88-124">**PR_RESOURCE_TYPE** Eintrag ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) stellt den Typ des Dienstanbieters dar. Dienstanbieter, die jedoch auf die entsprechende vordefinierte Konstante festlegen.</span><span class="sxs-lookup"><span data-stu-id="c2a88-124">**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) entry represents the type of service provider; service providers set it to the appropriate predefined constant.</span></span> <span data-ttu-id="c2a88-125">Gültige Werte sind MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER und "MAPI_AB_PROVIDER"..</span><span class="sxs-lookup"><span data-stu-id="c2a88-125">Valid values include MAPI_STORE_PROVIDER, MAPI_TRANSPORT_PROVIDER, and MAPI_AB_PROVIDER.</span></span>
  
<span data-ttu-id="c2a88-126">Eine andere Eigenschafteneintrag, der auf Message-Dienste und -Dienstanbieter angewendet wird, gibt die Optionen der Eintrag **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) an.</span><span class="sxs-lookup"><span data-stu-id="c2a88-126">Another property entry that applies to both message services and service providers, the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) entry indicates options.</span></span> <span data-ttu-id="c2a88-127">Die Einstellungen für diesen Eintrag-Eigenschaft können je nach den Dienstanbieter unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="c2a88-127">The settings for this property entry can differ depending on the service provider.</span></span> <span data-ttu-id="c2a88-128">Beispielsweise können einige Anbieter Nachricht **PR_RESOURCE_FLAGS** auf STATUS_NO_DEFAULT_STORE festgelegt, wenn sie nie als Standard-Informationsspeicher ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c2a88-128">For example, some message store providers might set **PR_RESOURCE_FLAGS** to STATUS_NO_DEFAULT_STORE if they can never operate as the default message store.</span></span> 
  
<span data-ttu-id="c2a88-129">Führen Sie die drei Beispiele für Service Provider Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="c2a88-129">Three examples of service provider sections follow.</span></span> <span data-ttu-id="c2a88-130">Im Abschnitt **[AB Provider]** ist für den Standard-Adressbuch-Dienst Bereich Service Provider.</span><span class="sxs-lookup"><span data-stu-id="c2a88-130">The **[AB Provider]** section is the service provider section for the Default Address Book service.</span></span> <span data-ttu-id="c2a88-131">Die Abschnitte **[MsgService Prov1]** und **[MsgService Prov2]** gehören zu meine eigenen Dienst. der erste ist ein Adressbuch Anbieterabschnitt und die zweite ist eine Nachrichtenspeicher Anbieterabschnitt.</span><span class="sxs-lookup"><span data-stu-id="c2a88-131">The **[MsgService Prov1]** and **[MsgService Prov2]** sections belong to My Own Service; the first is an address-book provider section and the second is a message-store provider section.</span></span> 
  
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


