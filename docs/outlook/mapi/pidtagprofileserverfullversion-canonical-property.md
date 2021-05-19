---
title: PidTagProfileServerFullVersion (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341601"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="3cd24-103">PidTagProfileServerFullVersion (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3cd24-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="3cd24-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cd24-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cd24-105">Gibt vollständige Versions- und Buildinformationen zu Microsoft Exchange Server, mit denen Konten in einem Profil verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="3cd24-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="3cd24-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="3cd24-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3cd24-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="3cd24-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="3cd24-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="3cd24-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3cd24-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="3cd24-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="3cd24-110">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="3cd24-110">Property type:</span></span>  <br/> |<span data-ttu-id="3cd24-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3cd24-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3cd24-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="3cd24-112">Area:</span></span>  <br/> |<span data-ttu-id="3cd24-113">MAPI-Profilkonfiguration</span><span class="sxs-lookup"><span data-stu-id="3cd24-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3cd24-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3cd24-114">Remarks</span></span>

<span data-ttu-id="3cd24-115">Ein Profil kann ein oder mehrere Konten angeben, die eine Verbindung mit Exchange Server herstellen, sie müssen jedoch mit demselben Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3cd24-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="3cd24-116">Versionen von Outlook vor Microsoft Office Outlook 2007 unterstützen diese Eigenschaft nicht.</span><span class="sxs-lookup"><span data-stu-id="3cd24-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="3cd24-117">Überprüfen Sie für diese Outlook, ob eine PR_PROFILE_SERVER_VERSION **[im](pidtagprofileserverversion-canonical-property.md)** Profil angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3cd24-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="3cd24-118">Wenn das aktive Postfach mit einer Exchange Server verbunden ist, speichert Outlook 2007 im allgemeinen vollständige Exchange Server Versionsinformationen in der **PR_PROFILE_SERVER_FULL_VERSION-Eigenschaft** im aktiven Profil.</span><span class="sxs-lookup"><span data-stu-id="3cd24-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="3cd24-119">Outlook speichert die Informationen in einer **EXCHANGE_STORE_VERSION_NUM,** die die Haupt- und Nebenversionsnummern sowie die Haupt- und Nebenversionsnummern enthält.</span><span class="sxs-lookup"><span data-stu-id="3cd24-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="3cd24-120">Wenn Sie z. B. die Exchange Server-Versions-ID **von 8.0.685.24** speichern möchten, ist die Hauptversionsnummer 8 und die Nebenversionsnummer 0, und die Hauptversionsnummer ist 685 und die Nebenversionsnummer 24.</span><span class="sxs-lookup"><span data-stu-id="3cd24-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="3cd24-121">Es ist **wahrscheinlich PR_PROFILE_SERVER_VERSION** oder **PR_PROFILE_SERVER_FULL_VERSION** in einem Profil vorhanden ist, aber es gibt keine Garantie, dass in einem Profil immer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3cd24-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="3cd24-122">Outlook schreibt erst in eine eigenschaft, wenn sie erfolgreich mit dem Objekt verbunden Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3cd24-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="3cd24-123">Im Outlook-Objektmodell können Sie die **ExchangeMailboxServerVersion-Eigenschaft** des **NameSpace-Objekts** verwenden, um die Version von Exchange Server zu finden, in der das aktive Postfach gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="3cd24-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="3cd24-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3cd24-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3cd24-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="3cd24-125">Protocol specifications</span></span>

<span data-ttu-id="3cd24-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="3cd24-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="3cd24-127">Stellt Eigenschaftensatzdefinitionen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3cd24-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3cd24-128">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="3cd24-128">Header files</span></span>

<span data-ttu-id="3cd24-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3cd24-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="3cd24-130">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="3cd24-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="3cd24-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3cd24-131">Mapitags.h</span></span>
  
> <span data-ttu-id="3cd24-132">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="3cd24-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3cd24-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3cd24-133">See also</span></span>



[<span data-ttu-id="3cd24-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3cd24-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3cd24-135">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="3cd24-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3cd24-136">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="3cd24-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3cd24-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="3cd24-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

