---
title: TNEF-Streamsyntax
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ce2b2497bd89f00ce7f063d3e482752fabfeb731
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594334"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="51aec-103">TNEF-Streamsyntax</span><span class="sxs-lookup"><span data-stu-id="51aec-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="51aec-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51aec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51aec-105">In diesem Thema wird ein Bakus-Nauer wie Beschreibung der Syntax der TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="51aec-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="51aec-106">In dieser Beschreibung werden nicht terminale Elemente, die eine weitere Definition kursiv angezeigt.</span><span class="sxs-lookup"><span data-stu-id="51aec-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="51aec-107">Konstanten und Literale Elemente sind fett dargestellt.</span><span class="sxs-lookup"><span data-stu-id="51aec-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="51aec-108">Sequences-Elemente sind in der Reihenfolge, in einer separaten Zeile aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="51aec-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="51aec-109">Das _Stream_ -Element umfasst beispielsweise die Konstante **TNEF_SIGNATURE**, gefolgt von einem _Schlüssel_, gefolgt von einem _Objekt_.</span><span class="sxs-lookup"><span data-stu-id="51aec-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="51aec-110">Wenn ein Element mehr als eine mögliche Implementierung aufweist, werden die alternativen in aufeinander folgenden Zeilen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="51aec-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="51aec-111">Ein _Objekt_ kann beispielsweise eine _Message_Seq_, eine _Message_Seq_ gefolgt von einer _Attach_Seq_oder nur ein _Attach_Seq_bestehen.</span><span class="sxs-lookup"><span data-stu-id="51aec-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="51aec-112">_TNEF_Stream:_</span><span class="sxs-lookup"><span data-stu-id="51aec-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="51aec-113">**TNEF_SIGNATURE** _Schlüssel_ _Objekt_</span><span class="sxs-lookup"><span data-stu-id="51aec-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="51aec-114">_Wichtige Punkte:_</span><span class="sxs-lookup"><span data-stu-id="51aec-114">_Key:_</span></span>
  
> <span data-ttu-id="51aec-115">eine ungleich NULL 16-Bit-Ganzzahl ohne Vorzeichen</span><span class="sxs-lookup"><span data-stu-id="51aec-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="51aec-116">TNEF aktiviert Transporten Generieren dieser Wert vor der Verwendung von TNEF-Implementierung zum Generieren der TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="51aec-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="51aec-117">_Objekt:_</span><span class="sxs-lookup"><span data-stu-id="51aec-117">_Object:_</span></span>
  
>  <span data-ttu-id="51aec-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="51aec-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="51aec-119">_Message_Seq:_</span><span class="sxs-lookup"><span data-stu-id="51aec-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="51aec-120">_AttTnefVersion AttTnefVersion Msg_Attribute_Seq AttTnefVersion AttMessageClass AttTnefVersion AttMessageClass Msg_Attribute_Seq AttMessageClass AttMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="51aec-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="51aec-121">_AttTnefVersion:_</span><span class="sxs-lookup"><span data-stu-id="51aec-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="51aec-122">**LVL_MESSAGE AttTnefVersion sizeof(ULONG)** **0 x 00010000** Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="51aec-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="51aec-123">_AttMessageClass:_</span><span class="sxs-lookup"><span data-stu-id="51aec-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="51aec-124">**LVL_MESSAGE attMessageClass** _Msg_class_length Msg_class_ Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="51aec-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="51aec-125">_Msg_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="51aec-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="51aec-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="51aec-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="51aec-127">_Msg_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="51aec-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="51aec-128">**LVL_MESSAGE** Attribut-ID-Attribut Länge Attributdaten Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="51aec-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="51aec-129">Attribut-ID ist eine der TNEF-Attribut Bezeichner, wie beispielsweise **AttSubject**.</span><span class="sxs-lookup"><span data-stu-id="51aec-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="51aec-130">Attribut Länge hat die Länge der Attributdaten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="51aec-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="51aec-131">Attributdaten ist das Attribut zugeordneten Daten.</span><span class="sxs-lookup"><span data-stu-id="51aec-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="51aec-132">_Attach_Seq:_</span><span class="sxs-lookup"><span data-stu-id="51aec-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="51aec-133">_AttRenddata AttRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="51aec-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="51aec-134">_AttRenddata:_</span><span class="sxs-lookup"><span data-stu-id="51aec-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="51aec-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** Renddata Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="51aec-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="51aec-136">Renddata ist die zugehörigen Daten für die **RENDDATA** -Struktur, die Renderinginformationen für die entsprechende Anlage enthält.</span><span class="sxs-lookup"><span data-stu-id="51aec-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="51aec-137">Die Struktur **RENDDATA** ist in die TNEF definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="51aec-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="51aec-138">_Att_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="51aec-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="51aec-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="51aec-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="51aec-140">_Att_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="51aec-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="51aec-141">**LVL_ATTACHMENT** Attribut-ID-Attribut Länge Attributdaten Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="51aec-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="51aec-142">Attribut-ID-Attribut Länge und Attributdaten haben die dieselbe Bedeutung wie für das Msg_Attribute-Element.</span><span class="sxs-lookup"><span data-stu-id="51aec-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

