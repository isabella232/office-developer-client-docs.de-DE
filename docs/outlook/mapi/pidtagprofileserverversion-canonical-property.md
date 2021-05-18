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
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286566"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="aeaac-103">PidTagProfileServerVersion (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="aeaac-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="aeaac-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aeaac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aeaac-105">Gibt Informationen zur Version von Microsoft Exchange Server an, mit denen Konten in einem Microsoft Outlook verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="aeaac-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="aeaac-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="aeaac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aeaac-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="aeaac-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="aeaac-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="aeaac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aeaac-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="aeaac-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="aeaac-110">Eigenschaftstyp:</span><span class="sxs-lookup"><span data-stu-id="aeaac-110">Property type:</span></span>  <br/> |<span data-ttu-id="aeaac-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="aeaac-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="aeaac-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="aeaac-112">Area:</span></span>  <br/> |<span data-ttu-id="aeaac-113">MAPI-Profilkonfiguration</span><span class="sxs-lookup"><span data-stu-id="aeaac-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aeaac-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aeaac-114">Remarks</span></span>

<span data-ttu-id="aeaac-115">Ein Profil kann ein oder mehrere Konten angeben, die eine Verbindung mit Exchange Server herstellen, sie müssen jedoch mit demselben Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="aeaac-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="aeaac-116">Versionen von Outlook vor Microsoft Office Outlook 2007 können in diese Eigenschaft schreiben, um Informationen zur Version von Exchange Server zu speichern, mit der das aktive Profil verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="aeaac-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="aeaac-117">Das Format der Versionsinformationen variiert jedoch für unterschiedliche Versionen Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="aeaac-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="aeaac-118">Beispielsweise speichert Outlook in **PR_PROFILE_SERVER_VERSION** den Dezimalwert 6944, um nur die Haupt buildnummer im Versionsbezeichner **6.5.6944.3** für Microsoft Exchange Server 2003 zu repräsentieren.</span><span class="sxs-lookup"><span data-stu-id="aeaac-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="aeaac-119">Für eine Exchange 2007 speichert Outlook die Hauptversionsnummer und die Hauptbaunummer in einer verkettten hexadezimalen Darstellung dieser Zahlen in der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="aeaac-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="aeaac-120">Eine Exchange Version 2007 von **8.0.685.24** hat die Hauptversionsnummer 8 und die Hauptbaunummer 685 im Dezimalformat.</span><span class="sxs-lookup"><span data-stu-id="aeaac-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="aeaac-121">Wenn Sie beide Zahlen in Hexadezimal konvertieren, erhalten 0x8 und 0x2AD.</span><span class="sxs-lookup"><span data-stu-id="aeaac-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="aeaac-122">Wenn Sie diese beiden Zahlen verketten, Outlook der Wert 0x82AD **in** PR_PROFILE_SERVER_VERSION in hexadezimaler Darstellung.</span><span class="sxs-lookup"><span data-stu-id="aeaac-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="aeaac-123">Outlook 2007 liest oder schreibt nicht in diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="aeaac-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="aeaac-124">Es unterstützt **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="aeaac-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="aeaac-125">Es ist **wahrscheinlich PR_PROFILE_SERVER_VERSION** oder **PR_PROFILE_SERVER_FULL_VERSION** in einem Profil vorhanden ist, aber es gibt keine Garantie, dass in einem Profil immer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="aeaac-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="aeaac-126">Outlook schreibt erst in eine eigenschaft, wenn sie erfolgreich mit dem Objekt verbunden Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="aeaac-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="aeaac-127">Im Outlook-Objektmodell können Sie die **ExchangeMailboxServerVersion-Eigenschaft** des **NameSpace-Objekts** verwenden, um die Version von Exchange Server zu finden, in der das aktive Postfach gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="aeaac-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="aeaac-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aeaac-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aeaac-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="aeaac-129">Protocol specifications</span></span>

<span data-ttu-id="aeaac-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aeaac-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aeaac-131">Stellt Eigenschaftensatzdefinitionen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="aeaac-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aeaac-132">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="aeaac-132">Header files</span></span>

<span data-ttu-id="aeaac-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aeaac-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="aeaac-134">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="aeaac-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="aeaac-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="aeaac-135">Mapitags.h</span></span>
  
> <span data-ttu-id="aeaac-136">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="aeaac-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aeaac-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aeaac-137">See also</span></span>



[<span data-ttu-id="aeaac-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aeaac-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aeaac-139">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="aeaac-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aeaac-140">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="aeaac-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aeaac-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="aeaac-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

