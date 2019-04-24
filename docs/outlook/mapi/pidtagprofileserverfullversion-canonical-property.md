---
title: Kanonische Pidtagprofileserverfullversion (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341601"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="24184-103">Kanonische Pidtagprofileserverfullversion (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="24184-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="24184-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24184-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24184-105">Gibt die vollständige Version und die Erstellung von Informationen zu Microsoft Exchange Server an, mit denen Konten in einem Profil verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="24184-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="24184-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="24184-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="24184-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="24184-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="24184-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="24184-108">Identifier:</span></span>  <br/> |<span data-ttu-id="24184-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="24184-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="24184-110">Eigenschafts:</span><span class="sxs-lookup"><span data-stu-id="24184-110">Property type:</span></span>  <br/> |<span data-ttu-id="24184-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="24184-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="24184-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="24184-112">Area:</span></span>  <br/> |<span data-ttu-id="24184-113">MAPI-Profilkonfiguration</span><span class="sxs-lookup"><span data-stu-id="24184-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24184-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24184-114">Remarks</span></span>

<span data-ttu-id="24184-115">Ein Profil kann ein oder mehrere Konten angeben, die eine Verbindung mit einem Exchange-Server herstellen, aber Sie müssen mit demselben Exchange-Server verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="24184-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="24184-116">Versionen von Outlook vor Microsoft Office Outlook 2007 unterstützen diese Eigenschaft nicht.</span><span class="sxs-lookup"><span data-stu-id="24184-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="24184-117">Überprüfen Sie für diese Versionen von Outlook, ob **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** im Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="24184-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="24184-118">Wenn das aktive Postfach mit einem Exchange-Server verbunden ist, speichert Outlook 2007 vollständige Exchange Server-Versionsinformationen in der **PR_PROFILE_SERVER_FULL_VERSION** -Eigenschaft im aktiven Profil.</span><span class="sxs-lookup"><span data-stu-id="24184-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="24184-119">Outlook speichert die Informationen in einer **EXCHANGE_STORE_VERSION_NUM** -Struktur, die die Haupt-und Nebenversionsnummern sowie die Haupt-und Nebenversionen enthält.</span><span class="sxs-lookup"><span data-stu-id="24184-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="24184-120">Um beispielsweise die Exchange Server-Versionskennung von **8.0.685.24**zu speichern, ist die Hauptversionsnummer 8, und die Versionsnummer der Nebenversion ist 0, und die Haupt buildnummer lautet 685 und die Minor Build number ist 24.</span><span class="sxs-lookup"><span data-stu-id="24184-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="24184-121">Nur eines von **PR_PROFILE_SERVER_VERSION** oder **PR_PROFILE_SERVER_FULL_VERSION** ist wahrscheinlich in einem Profil vorhanden, aber es gibt keine Garantie, dass es in einem Profil immer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="24184-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="24184-122">Outlook schreibt in keiner der Eigenschaften, bis eine erfolgreiche Verbindung mit dem Exchange-Server hergestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="24184-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="24184-123">Im Outlook-Objektmodell können Sie die **ExchangeMailboxServerVersion** -Eigenschaft des **Namespace** -Objekts verwenden, um die Version von Exchange Server zu suchen, auf der das aktive Postfach gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="24184-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="24184-124">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="24184-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="24184-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="24184-125">Protocol specifications</span></span>

<span data-ttu-id="24184-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="24184-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="24184-127">Stellt Definitionen für Eigenschaftensätze bereit.</span><span class="sxs-lookup"><span data-stu-id="24184-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="24184-128">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="24184-128">Header files</span></span>

<span data-ttu-id="24184-129">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="24184-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="24184-130">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="24184-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="24184-131">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="24184-131">Mapitags.h</span></span>
  
> <span data-ttu-id="24184-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="24184-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24184-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24184-133">See also</span></span>



[<span data-ttu-id="24184-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24184-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="24184-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="24184-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="24184-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="24184-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="24184-137">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="24184-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

