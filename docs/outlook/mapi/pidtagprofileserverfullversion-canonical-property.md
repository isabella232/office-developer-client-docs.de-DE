---
title: Kanonische PidTagProfileServerFullVersion-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 284b4b451a31a9478caf31fe855d38bfeab2caf3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794819"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="41caf-103">Kanonische PidTagProfileServerFullVersion-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="41caf-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="41caf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41caf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41caf-105">Gibt die vollständige Angaben zu Version und Build über die Microsoft Exchange Server-Konten in einem Profil verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="41caf-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="41caf-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="41caf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="41caf-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="41caf-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="41caf-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="41caf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="41caf-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="41caf-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="41caf-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="41caf-110">Property type:</span></span>  <br/> |<span data-ttu-id="41caf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="41caf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="41caf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="41caf-112">Area:</span></span>  <br/> |<span data-ttu-id="41caf-113">MAPI-Profil-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="41caf-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41caf-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="41caf-114">Remarks</span></span>

<span data-ttu-id="41caf-115">Ein Profil kann eine oder mehrere Konten, die mit einem Exchange-Server verbunden angeben, jedoch müssen die gleichen Exchange-Server hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="41caf-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="41caf-116">Diese Eigenschaft wird von Outlook-Versionen vor Microsoft Office Outlook 2007 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="41caf-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="41caf-117">Überprüfen Sie für diese Versionen von Outlook das Vorhandensein des **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** im Profil.</span><span class="sxs-lookup"><span data-stu-id="41caf-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="41caf-118">Wenn das aktive Postfach mit einem Exchange-Server verbunden ist, speichert Outlook 2007 umfassende Informationen zur Version von Exchange Server in der Regel in der **PR_PROFILE_SERVER_FULL_VERSION** -Eigenschaft in das aktive Profil.</span><span class="sxs-lookup"><span data-stu-id="41caf-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="41caf-119">Outlook speichert die Informationen in eine **EXCHANGE_STORE_VERSION_NUM** -Struktur, die Haupt- und Hilfsintervalle Versionsnummern und die Haupt- und Hilfsintervalle Buildnummern enthält.</span><span class="sxs-lookup"><span data-stu-id="41caf-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="41caf-120">Beispielsweise, um die Exchange Server-Version-Bezeichner des **8.0.685.24**gespeichert werden sollen, ist die Nummer der Hauptversion 8 und Nebenversionsnummer ist 0, und die wichtigsten Buildnummer wird 685 und minor Buildnummer 24 ist.</span><span class="sxs-lookup"><span data-stu-id="41caf-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="41caf-121">Nur eine der **PR_PROFILE_SERVER_VERSION** oder **PR_PROFILE_SERVER_FULL_VERSION** wahrscheinlich in einem Profil vorhanden ist, aber es ist nicht gewährleistet, dass entweder immer in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="41caf-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="41caf-122">Outlook wird nicht auf eine der Eigenschaften geschrieben, bis er erfolgreich mit dem Exchange-Server verbunden hat.</span><span class="sxs-lookup"><span data-stu-id="41caf-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="41caf-123">Im Outlook-Objektmodell können Sie die **ExchangeMailboxServerVersion** -Eigenschaft des **NameSpace** -Objekts verwenden, um die Version von Exchange Server zu erhalten, auf dem das aktuelle Postfach gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="41caf-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="41caf-124">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="41caf-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="41caf-125">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="41caf-125">Protocol specifications</span></span>

<span data-ttu-id="41caf-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="41caf-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="41caf-127">Enthält Eigenschaftendefinitionen an.</span><span class="sxs-lookup"><span data-stu-id="41caf-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="41caf-128">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="41caf-128">Header files</span></span>

<span data-ttu-id="41caf-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="41caf-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="41caf-130">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="41caf-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="41caf-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="41caf-131">Mapitags.h</span></span>
  
> <span data-ttu-id="41caf-132">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="41caf-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="41caf-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41caf-133">See also</span></span>



[<span data-ttu-id="41caf-134">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41caf-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="41caf-135">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="41caf-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="41caf-136">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="41caf-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="41caf-137">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="41caf-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

