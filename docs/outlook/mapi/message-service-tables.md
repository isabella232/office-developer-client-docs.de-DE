---
title: Nachrichtendiensttabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 569c1bd7ee2f4ac6c321f234be2954a57715549b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576669"
---
# <a name="message-service-tables"></a><span data-ttu-id="d99c3-103">Nachrichtendiensttabellen</span><span class="sxs-lookup"><span data-stu-id="d99c3-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="d99c3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d99c3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d99c3-105">Die Nachricht Service-Tabelle enthält Informationen zu den Diensten Nachricht im aktuellen Profil.</span><span class="sxs-lookup"><span data-stu-id="d99c3-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="d99c3-106">Es wird eine Meldung-Service-Tabelle für jede MAPI-Sitzung, MAPI Implementierung und Verwendung von speziellen-Clientanwendungen, die Konfiguration unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d99c3-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="d99c3-107">Die Nachricht Service-Tabelle ist eine statische Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d99c3-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="d99c3-108">Clientzugriff durch Aufrufen der Methode [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) die Tabelle der Dienste.</span><span class="sxs-lookup"><span data-stu-id="d99c3-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="d99c3-109">Die folgenden Eigenschaften bilden die erforderliche Spalte in der Tabelle der Dienste festgelegt:</span><span class="sxs-lookup"><span data-stu-id="d99c3-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d99c3-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d99c3-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d99c3-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d99c3-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d99c3-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d99c3-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d99c3-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d99c3-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d99c3-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d99c3-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d99c3-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d99c3-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d99c3-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d99c3-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="d99c3-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d99c3-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="d99c3-118">**PR_DISPLAY_NAME** ist der Anzeigename für den Dienst und die Schlüsselspalte der standardmäßigen sortieren.</span><span class="sxs-lookup"><span data-stu-id="d99c3-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="d99c3-119">**PR_INSTANCE_KEY** dient als Index-Spalte für die Tabelle, die eine Zeile eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d99c3-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="d99c3-120">**PR_RESOURCE_FLAGS** wird die Nachricht Service-Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d99c3-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="d99c3-121">**PR_SERVICE_DLL_NAME** ist der Name der DLL, die die Implementierung der Service Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="d99c3-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="d99c3-122">**PR_SERVICE_ENTRY_NAME** ist der Name der Messagingdiensts Eintrag Point-Funktion, die den [MSGSERVICEENTRY](msgserviceentry.md) Prototyp entspricht.</span><span class="sxs-lookup"><span data-stu-id="d99c3-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="d99c3-123">**PR_SERVICE_NAME** ist eine erforderliche Eintrag im Abschnitt **[Services]** in MAPISVC.INF.</span><span class="sxs-lookup"><span data-stu-id="d99c3-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="d99c3-124">Der Wert für diese Eigenschaft wird nie geändert oder lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="d99c3-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="d99c3-125">**PR_SERVICE_NAME** kann verwendet werden, um den Dienst programmgesteuert zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d99c3-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="d99c3-126">**PR_SERVICE_SUPPORT_FILES** ist eine Liste von Dateien, die mit dem Nachrichtendienst installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="d99c3-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="d99c3-127">**PR_SERVICE_UID** ist ein eindeutiger Bezeichner für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="d99c3-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d99c3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d99c3-128">See also</span></span>



[<span data-ttu-id="d99c3-129">MAPI-Tabellen</span><span class="sxs-lookup"><span data-stu-id="d99c3-129">MAPI Tables</span></span>](mapi-tables.md)

