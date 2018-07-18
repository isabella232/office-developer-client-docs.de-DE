---
title: PidTagMessageDownloadTime (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageDownloadTime
api_type:
- HeaderDef
ms.assetid: f0d34dd6-7ddb-4843-b848-c89923ff80cc
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b47d104ade6a7d23f5630d15697b330360d027b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794603"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="8d439-103">PidTagMessageDownloadTime (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8d439-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="8d439-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8d439-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8d439-105">Enthält die geschätzte Zeit bis zum Laden Sie einer Nachricht von einem Remoteserver zu einem lokalen Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="8d439-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d439-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8d439-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8d439-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="8d439-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="8d439-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="8d439-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8d439-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="8d439-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="8d439-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8d439-110">Data type:</span></span>  <br/> |<span data-ttu-id="8d439-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8d439-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8d439-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8d439-112">Area:</span></span>  <br/> |<span data-ttu-id="8d439-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="8d439-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d439-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d439-114">Remarks</span></span>

<span data-ttu-id="8d439-115">Diese Eigenschaft wird in Sekunden ausgedrückt und stellt die bestmögliche Schätzung der Zeit an einen remote-Transport-Anbieter zu eine bestimmte Nachricht von seinem aktuellen Speicherort auf einen Nachrichtenspeicher herunterladen lokalen an dem Client, die das Anzeigen des Ordners Kopfzeile dauert.</span><span class="sxs-lookup"><span data-stu-id="8d439-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="8d439-116">Der remote Adressbuchhierarchie berechnet den Wert für diese Eigenschaft in der Regel durch Dividieren des Werts der Eigenschaft **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) durch die Geschwindigkeit der Communications-Verknüpfung in Byte pro Sekunde.</span><span class="sxs-lookup"><span data-stu-id="8d439-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="8d439-117">Wenn der Anbieter die Downloadzeit, z. B., wenn er die Übertragungsrate nicht kennt berechnen kann nicht sollte einen **PT_ERROR** -Wert wie **MAPI_E_NO_SUPPORT** für diese Spalte in der Kopfzeile Ordner Inhaltstabelle Büroplan.</span><span class="sxs-lookup"><span data-stu-id="8d439-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8d439-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8d439-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8d439-119">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="8d439-119">Header files</span></span>

<span data-ttu-id="8d439-120">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8d439-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="8d439-121">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8d439-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="8d439-122">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8d439-122">Mapitags.h</span></span>
  
> <span data-ttu-id="8d439-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="8d439-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d439-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d439-124">See also</span></span>



[<span data-ttu-id="8d439-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d439-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8d439-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8d439-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8d439-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8d439-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8d439-128">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8d439-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

