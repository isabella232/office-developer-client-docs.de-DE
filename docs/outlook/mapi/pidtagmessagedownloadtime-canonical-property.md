---
title: Kanonische Pidtagmessagedownloadtime (-Eigenschaft
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
ms.openlocfilehash: 8078d31af497a437c983da7447a0aebbdfb643fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325676"
---
# <a name="pidtagmessagedownloadtime-canonical-property"></a><span data-ttu-id="4f317-103">Kanonische Pidtagmessagedownloadtime (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4f317-103">PidTagMessageDownloadTime Canonical Property</span></span>

  
  
<span data-ttu-id="4f317-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f317-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f317-105">Enthält die geschätzte Zeit zum Herunterladen einer Nachricht von einem Remoteserver zu einem lokalen Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="4f317-105">Contains the estimated time to download a message from a remote server to a local message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4f317-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="4f317-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4f317-107">PR_MESSAGE_DOWNLOAD_TIME</span><span class="sxs-lookup"><span data-stu-id="4f317-107">PR_MESSAGE_DOWNLOAD_TIME</span></span>  <br/> |
|<span data-ttu-id="4f317-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="4f317-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4f317-109">0x0E18</span><span class="sxs-lookup"><span data-stu-id="4f317-109">0x0E18</span></span>  <br/> |
|<span data-ttu-id="4f317-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="4f317-110">Data type:</span></span>  <br/> |<span data-ttu-id="4f317-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4f317-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4f317-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="4f317-112">Area:</span></span>  <br/> |<span data-ttu-id="4f317-113">Allgemeine Nachrichtenübermittlung</span><span class="sxs-lookup"><span data-stu-id="4f317-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4f317-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f317-114">Remarks</span></span>

<span data-ttu-id="4f317-115">Diese Eigenschaft wird in Sekunden ausgedrückt und stellt die beste Schätzung der Zeit dar, die ein Remote Transportanbieter zum Herunterladen einer bestimmten Nachricht vom aktuellen Speicherort zum lokalen Nachrichtenspeicher des Clients zum Anzeigen des Kopfzeilen Ordners benötigen würde.</span><span class="sxs-lookup"><span data-stu-id="4f317-115">This property is expressed in seconds and represents the best estimate of the time it would take a remote transport provider to download a given message from its current location to a message store local to the client viewing the header folder.</span></span> <span data-ttu-id="4f317-116">Der Remote Transportanbieter berechnet in der Regel den Wert für diese Eigenschaft, indem der Wert der **PR_MESSAGE_SIZE** ([pidtagmessagesize (](pidtagmessagesize-canonical-property.md))-Eigenschaft durch die Geschwindigkeit der Kommunikationsverbindung in Bytes pro Sekunde geteilt wird.</span><span class="sxs-lookup"><span data-stu-id="4f317-116">The remote transport provider typically calculates the value for this property by dividing the value of the **PR_MESSAGE_SIZE** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md)) property by the speed of the communications link in bytes per second.</span></span> <span data-ttu-id="4f317-117">Wenn der Anbieter die Downloadzeit nicht berechnen kann, beispielsweise wenn er die Verbindungsgeschwindigkeit nicht kennt, sollte er einen **PT_ERROR** -Wert wie **MAPI_E_NO_SUPPORT** für diese Spalte in der Tabelle mit den Kopfzeilen Ordnern liefern.</span><span class="sxs-lookup"><span data-stu-id="4f317-117">If the provider cannot calculate the download time, for example if it does not know the link speed, it should furnish a **PT_ERROR** value such as **MAPI_E_NO_SUPPORT** for this column in the header folder contents table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="4f317-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4f317-118">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="4f317-119">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="4f317-119">Header files</span></span>

<span data-ttu-id="4f317-120">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="4f317-120">Mapidefs.h</span></span>
  
> <span data-ttu-id="4f317-121">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="4f317-121">Provides data type definitions.</span></span>
    
<span data-ttu-id="4f317-122">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="4f317-122">Mapitags.h</span></span>
  
> <span data-ttu-id="4f317-123">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="4f317-123">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4f317-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f317-124">See also</span></span>



[<span data-ttu-id="4f317-125">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f317-125">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4f317-126">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f317-126">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4f317-127">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="4f317-127">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4f317-128">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="4f317-128">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

