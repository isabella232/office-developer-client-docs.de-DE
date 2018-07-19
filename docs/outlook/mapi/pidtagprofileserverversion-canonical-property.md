---
title: PidTagProfileServerVersion (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 571ac25d6bc738f8289e3019c342820682d08c28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794816"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="915eb-103">PidTagProfileServerVersion (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="915eb-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="915eb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="915eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="915eb-105">Gibt Informationen über die Version von Microsoft Exchange Server-Konten in einem Microsoft Outlook-Profil verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="915eb-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="915eb-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="915eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="915eb-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="915eb-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="915eb-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="915eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="915eb-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="915eb-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="915eb-110">Der Eigenschaftentyp:</span><span class="sxs-lookup"><span data-stu-id="915eb-110">Property type:</span></span>  <br/> |<span data-ttu-id="915eb-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="915eb-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="915eb-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="915eb-112">Area:</span></span>  <br/> |<span data-ttu-id="915eb-113">MAPI-Profil-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="915eb-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="915eb-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="915eb-114">Remarks</span></span>

<span data-ttu-id="915eb-115">Ein Profil kann eine oder mehrere Konten, die mit einem Exchange-Server verbunden angeben, jedoch müssen die gleichen Exchange-Server hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="915eb-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="915eb-116">Outlook-Versionen vor Microsoft Office Outlook 2007 können Schreiben auf diese Eigenschaft zum Speichern von Informationen zur Version von Exchange Server mit dem das aktive Profil verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="915eb-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="915eb-117">Das Format der die Versionsinformationen ändert sich jedoch für die verschiedenen Versionen von Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="915eb-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="915eb-118">Beispielsweise Buildnummer Outlook-Speicher in **PR_PROFILE_SERVER_VERSION** den Dezimalwert 6944 nur die wichtigsten dargestellt in der Versionsbezeichner des **6.5.6944.3** für Microsoft Exchange Server 2003.</span><span class="sxs-lookup"><span data-stu-id="915eb-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="915eb-119">Für eine Exchange 2007-Verbindung Outlook speichert die Nummer der Hauptversion und die Major-Buildnummer in einer verketteten hexadezimale Darstellung dieser Zahlen in der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="915eb-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="915eb-120">Ein Exchange 2007-Version-Bezeichner des **8.0.685.24** hat Hauptversionsnummer 8 und eine Haupt-Buildnummer 685 Dezimal.</span><span class="sxs-lookup"><span data-stu-id="915eb-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="915eb-121">Konvertieren von beiden Zahlen in eine Hexadezimalzahl, erhalten Sie 0 x 8 und 0x2AD.</span><span class="sxs-lookup"><span data-stu-id="915eb-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="915eb-122">Diese beiden Zahlen verketten, speichert Outlook den Wert 0x82AD in **PR_PROFILE_SERVER_VERSION** , im Hexadezimal-Darstellung.</span><span class="sxs-lookup"><span data-stu-id="915eb-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="915eb-123">Outlook 2007 nicht lesen oder Schreiben in diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="915eb-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="915eb-124">**[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)** unterstützt.</span><span class="sxs-lookup"><span data-stu-id="915eb-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="915eb-125">Nur eine der **PR_PROFILE_SERVER_VERSION** oder **PR_PROFILE_SERVER_FULL_VERSION** wahrscheinlich in einem Profil vorhanden ist, aber es ist nicht gewährleistet, dass entweder immer in einem Profil vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="915eb-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="915eb-126">Outlook wird nicht auf eine der Eigenschaften geschrieben, bis er erfolgreich mit dem Exchange-Server verbunden hat.</span><span class="sxs-lookup"><span data-stu-id="915eb-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="915eb-127">Im Outlook-Objektmodell können Sie die **ExchangeMailboxServerVersion** -Eigenschaft des **NameSpace** -Objekts verwenden, um die Version von Exchange Server zu erhalten, auf dem das aktuelle Postfach gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="915eb-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="915eb-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="915eb-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="915eb-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="915eb-129">Protocol specifications</span></span>

<span data-ttu-id="915eb-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="915eb-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="915eb-131">Enthält Eigenschaftendefinitionen an.</span><span class="sxs-lookup"><span data-stu-id="915eb-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="915eb-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="915eb-132">Header files</span></span>

<span data-ttu-id="915eb-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="915eb-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="915eb-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="915eb-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="915eb-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="915eb-135">Mapitags.h</span></span>
  
> <span data-ttu-id="915eb-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="915eb-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="915eb-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="915eb-137">See also</span></span>



[<span data-ttu-id="915eb-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="915eb-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="915eb-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="915eb-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="915eb-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="915eb-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="915eb-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="915eb-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

