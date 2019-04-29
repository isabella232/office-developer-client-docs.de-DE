---
title: Nachrichtendienst Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422495"
---
# <a name="message-service-tables"></a><span data-ttu-id="388ce-103">Nachrichtendienst Tabellen</span><span class="sxs-lookup"><span data-stu-id="388ce-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="388ce-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="388ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="388ce-105">Die Nachrichtendienst Tabelle enthält Informationen zu den Nachrichtendiensten im aktuellen Profil.</span><span class="sxs-lookup"><span data-stu-id="388ce-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="388ce-106">Es gibt eine Nachrichtendienst Tabelle für jede MAPI-Sitzung, die von MAPI implementiert und von speziellen Clientanwendungen verwendet wird, die Konfigurationsunterstützung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="388ce-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="388ce-107">Die Nachrichtendienst Tabelle ist eine statische Tabelle.</span><span class="sxs-lookup"><span data-stu-id="388ce-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="388ce-108">Clients greifen auf die Nachrichtendienst Tabelle zu, indem Sie die [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="388ce-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="388ce-109">Die folgenden Eigenschaften stellen den erforderlichen Spaltensatz in der Nachrichtendienst Tabelle dar:</span><span class="sxs-lookup"><span data-stu-id="388ce-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="388ce-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="388ce-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="388ce-111">**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="388ce-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="388ce-112">**PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="388ce-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="388ce-113">**PR_SERVICE_DLL_NAME** ([Pidtagservicedllname (](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="388ce-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="388ce-114">**PR_SERVICE_ENTRY_NAME** ([Pidtagserviceentryname (](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="388ce-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="388ce-115">**PR_SERVICE_NAME** ([Pidtagservicename (](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="388ce-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="388ce-116">**PR_SERVICE_SUPPORT_FILES** ([Pidtagservicesupportfiles (](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="388ce-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="388ce-117">**PR_SERVICE_UID** ([Pidtagserviceuid (](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="388ce-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="388ce-118">**PR_DISPLAY_NAME** ist der Anzeige Name für den Nachrichtendienst und die standardmäßige Sortierschlüsselspalte.</span><span class="sxs-lookup"><span data-stu-id="388ce-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="388ce-119">**PR_INSTANCE_KEY** dient als Indexspalte für die Tabelle, um eine Zeile eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="388ce-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="388ce-120">**PR_RESOURCE_FLAGS** beschreibt die Funktionen des Nachrichtendiensts.</span><span class="sxs-lookup"><span data-stu-id="388ce-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="388ce-121">**PR_SERVICE_DLL_NAME** ist der Name der dll, die die Implementierung des Nachrichtendiensts enthält.</span><span class="sxs-lookup"><span data-stu-id="388ce-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="388ce-122">**PR_SERVICE_ENTRY_NAME** ist der Name der Einstiegspunktfunktion des Nachrichtendiensts, die dem [MSGSERVICEENTRY](msgserviceentry.md) -Prototyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="388ce-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="388ce-123">**PR_SERVICE_NAME** ist ein erforderlicher Eintrag im Abschnitt **[Dienste]** in MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="388ce-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="388ce-124">Der Wert für diese Eigenschaft wird nie geändert oder lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="388ce-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="388ce-125">**PR_SERVICE_NAME** kann zum programmgesteuerten Identifizieren des Nachrichtendiensts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="388ce-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="388ce-126">**PR_SERVICE_SUPPORT_FILES** ist eine Liste der Dateien, die mit dem Nachrichtendienst installiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="388ce-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="388ce-127">**PR_SERVICE_UID** ist ein eindeutiger Bezeichner für den Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="388ce-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="388ce-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="388ce-128">See also</span></span>



[<span data-ttu-id="388ce-129">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="388ce-129">MAPI Tables</span></span>](mapi-tables.md)

