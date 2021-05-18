---
title: '#A0'
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1353d494-c266-4715-afe7-14543a1bbe1b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 12d2a92ff80897456707c7ab8af8f704605c85d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423027"
---
# <a name="tnef-stream-syntax"></a><span data-ttu-id="30e18-103">#A0</span><span class="sxs-lookup"><span data-stu-id="30e18-103">TNEF Stream Syntax</span></span>

  
  
<span data-ttu-id="30e18-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30e18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30e18-105">In diesem Thema wird eine Bakus-Nauer beschreibung der TNEF-Streamsyntax beschrieben.</span><span class="sxs-lookup"><span data-stu-id="30e18-105">This topic presents a Bakus-Nauer like description of the TNEF stream syntax.</span></span> <span data-ttu-id="30e18-106">In dieser Beschreibung sind nicht terminale Elemente, die eine weitere Definition haben, italisch.</span><span class="sxs-lookup"><span data-stu-id="30e18-106">In this description, nonterminal elements that have a further definition are in italics.</span></span> <span data-ttu-id="30e18-107">Konstanten und Literalelemente sind fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="30e18-107">Constants and literal items are in bold.</span></span> <span data-ttu-id="30e18-108">Sequenzen von Elementen werden in der Reihenfolge einer einzelnen Zeile aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="30e18-108">Sequences of elements are listed in order on a single line.</span></span> <span data-ttu-id="30e18-109">Das _Stream-Element_ besteht z. B. aus der TNEF_SIGNATURE **,** gefolgt von einem _Key_-Element, gefolgt von einem _Object -Element._</span><span class="sxs-lookup"><span data-stu-id="30e18-109">For example, the  _Stream_ item consists of the constant **TNEF_SIGNATURE**, followed by a  _Key_, followed by an  _Object_.</span></span> <span data-ttu-id="30e18-110">Wenn ein Element über mehrere mögliche Implementierungen verfügt, werden die Alternativen in aufeinander folgenden Zeilen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="30e18-110">When an item has more than one possible implementation, the alternatives are listed on consecutive lines.</span></span> <span data-ttu-id="30e18-111">Ein Objekt  kann z. B. aus einer  Message_Seq _,_ einer Message_Seq gefolgt von einer Attach_Seq _oder_ einfach einer Attach_Seq _._</span><span class="sxs-lookup"><span data-stu-id="30e18-111">For example, an  _Object_ can consist of a  _Message_Seq_, a  _Message_Seq_ followed by an  _Attach_Seq_, or just an  _Attach_Seq_.</span></span>
  
 <span data-ttu-id="30e18-112">_TNEF_Stream:_</span><span class="sxs-lookup"><span data-stu-id="30e18-112">_TNEF_Stream:_</span></span>
  
> <span data-ttu-id="30e18-113">**TNEF_SIGNATURE** _Key-Objekt_ </span><span class="sxs-lookup"><span data-stu-id="30e18-113">**TNEF_SIGNATURE** _Key_ _Object_</span></span>
    
 <span data-ttu-id="30e18-114">_Schlüssel:_</span><span class="sxs-lookup"><span data-stu-id="30e18-114">_Key:_</span></span>
  
> <span data-ttu-id="30e18-115">eine nicht signierte 16-Bit-Ganzzahl ungleich 16 Bit</span><span class="sxs-lookup"><span data-stu-id="30e18-115">a nonzero 16-bit unsigned integer</span></span>
    
<span data-ttu-id="30e18-116">TNEF-aktivierte Transporte generieren diesen Wert, bevor die TNEF-Implementierung zum Generieren eines TNEF-Datenstroms verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="30e18-116">TNEF enabled transports generate this value before using the TNEF implementation to generate a TNEF stream.</span></span>
  
 <span data-ttu-id="30e18-117">_Objekt:_</span><span class="sxs-lookup"><span data-stu-id="30e18-117">_Object:_</span></span>
  
>  <span data-ttu-id="30e18-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span><span class="sxs-lookup"><span data-stu-id="30e18-118">_Message_Seq Message_Seq Attach_Seq Attach_Seq_</span></span>
    
 <span data-ttu-id="30e18-119">_Message_Seq:_</span><span class="sxs-lookup"><span data-stu-id="30e18-119">_Message_Seq:_</span></span>
  
>  <span data-ttu-id="30e18-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="30e18-120">_attTnefVersion attTnefVersion Msg_Attribute_Seq attTnefVersion attMessageClass attTnefVersion attMessageClass Msg_Attribute_Seq attMessageClass attMessageClass Msg_Attribute_Seq Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="30e18-121">_attTnefVersion:_</span><span class="sxs-lookup"><span data-stu-id="30e18-121">_attTnefVersion:_</span></span>
  
> <span data-ttu-id="30e18-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="30e18-122">**LVL_MESSAGE attTnefVersion sizeof(ULONG)** **0x00010000** checksum</span></span> 
    
 <span data-ttu-id="30e18-123">_attMessageClass:_</span><span class="sxs-lookup"><span data-stu-id="30e18-123">_attMessageClass:_</span></span>
  
> <span data-ttu-id="30e18-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="30e18-124">**LVL_MESSAGE attMessageClass** _msg_class_length msg_class_ checksum</span></span> 
    
 <span data-ttu-id="30e18-125">_Msg_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="30e18-125">_Msg_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="30e18-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="30e18-126">_Msg_Attribute Msg_Attribute Msg_Attribute_Seq_</span></span>
    
 <span data-ttu-id="30e18-127">_Msg_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="30e18-127">_Msg_Attribute:_</span></span>
  
> <span data-ttu-id="30e18-128">**LVL_MESSAGE** attribut-ID attribut-length attribut-data checksum</span><span class="sxs-lookup"><span data-stu-id="30e18-128">**LVL_MESSAGE** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="30e18-129">Attribut-ID ist eine der TNEF-Attributbezeichner, z. B. **attSubject**.</span><span class="sxs-lookup"><span data-stu-id="30e18-129">Attribute-ID is one of the TNEF attribute identifiers, such as **attSubject**.</span></span> <span data-ttu-id="30e18-130">Attributlänge ist die Länge in Bytes der Attributdaten.</span><span class="sxs-lookup"><span data-stu-id="30e18-130">Attribute-length is the length in bytes of the attribute data.</span></span> <span data-ttu-id="30e18-131">Attributdaten sind die Daten, die dem Attribut zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="30e18-131">Attribute-data is the data associated with the attribute.</span></span>
  
 <span data-ttu-id="30e18-132">_Attach_Seq:_</span><span class="sxs-lookup"><span data-stu-id="30e18-132">_Attach_Seq:_</span></span>
  
>  <span data-ttu-id="30e18-133">_attRenddata attRenddata Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="30e18-133">_attRenddata attRenddata Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="30e18-134">_attRenddata:_</span><span class="sxs-lookup"><span data-stu-id="30e18-134">_attRenddata:_</span></span>
  
> <span data-ttu-id="30e18-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span><span class="sxs-lookup"><span data-stu-id="30e18-135">**LVL_ATTACHMENT attRenddata** **sizeof(RENDDATA)** renddata checksum</span></span> 
    
<span data-ttu-id="30e18-136">Renddata sind die Der **RENDDATA-Struktur** zugeordneten Daten, die die Renderinginformationen für die entsprechende Anlage enthalten.</span><span class="sxs-lookup"><span data-stu-id="30e18-136">Renddata is the data associated with the **RENDDATA** structure that contains the rendering information for the corresponding attachment.</span></span> <span data-ttu-id="30e18-137">Die **RENDDATA-Struktur** ist im TNEF definiert. H-Headerdatei.</span><span class="sxs-lookup"><span data-stu-id="30e18-137">The **RENDDATA** structure is defined in the TNEF.H header file.</span></span> 
  
 <span data-ttu-id="30e18-138">_Att_Attribute_Seq:_</span><span class="sxs-lookup"><span data-stu-id="30e18-138">_Att_Attribute_Seq:_</span></span>
  
>  <span data-ttu-id="30e18-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span><span class="sxs-lookup"><span data-stu-id="30e18-139">_Att_Attribute Att_Attribute Att_Attribute_Seq_</span></span>
    
 <span data-ttu-id="30e18-140">_Att_Attribute:_</span><span class="sxs-lookup"><span data-stu-id="30e18-140">_Att_Attribute:_</span></span>
  
> <span data-ttu-id="30e18-141">**LVL_ATTACHMENT** attribut-ID attribut-length attribut-data checksum</span><span class="sxs-lookup"><span data-stu-id="30e18-141">**LVL_ATTACHMENT** attribute-ID attribute-length attribute-data checksum</span></span> 
    
<span data-ttu-id="30e18-142">Attribut-ID, Attributlänge und Attributdaten haben die gleichen Bedeutungen wie für das Msg_Attribute Element.</span><span class="sxs-lookup"><span data-stu-id="30e18-142">Attribute-ID, attribute-length, and attribute-data have the same meanings as for the Msg_Attribute item.</span></span>
  

