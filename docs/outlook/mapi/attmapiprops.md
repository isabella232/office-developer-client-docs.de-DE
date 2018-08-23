---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 72f252791e374ed4b9b2a40c9b151ef2b91fefe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588055"
---
# <a name="attmapiprops"></a><span data-ttu-id="a4750-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="a4750-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="a4750-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4750-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4750-105">Das Attribut **AttMAPIProps** werden spezielle zum Codieren von MAPI-Eigenschaften, die kein Gegenstück in der Gruppe von vorhandenen TNEF benutzerdefinierte Attribute verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="a4750-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="a4750-106">Die Attributdaten ist ein gezählte festgelegten End-to-End-MAPI-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="a4750-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="a4750-107">Das Format dieser Codierung, die für jeden Satz von MAPI-Eigenschaften werden kann, ist wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a4750-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="a4750-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="a4750-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="a4750-109">Eigenschaft Count _Property_Value..._</span><span class="sxs-lookup"><span data-stu-id="a4750-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="a4750-110">Gibt an, der Wert der Eigenschaft Count _Property_Value_ Elemente muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a4750-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="a4750-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="a4750-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="a4750-112">Eigenschafts-Tag _Property_property-Tag _Proptag_Name-Eigenschaft_</span><span class="sxs-lookup"><span data-stu-id="a4750-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="a4750-113">Das Eigenschaft-Tag ist einfach den Wert der Eigenschaft-ID, wie etwa 0x0037001F für **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a4750-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="a4750-114">_Eigenschaft:_</span><span class="sxs-lookup"><span data-stu-id="a4750-114">_Property:_</span></span>
  
>  <span data-ttu-id="a4750-115">_Wert_ Wert-Count _Value..._</span><span class="sxs-lookup"><span data-stu-id="a4750-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="a4750-116">_Wert:_</span><span class="sxs-lookup"><span data-stu-id="a4750-116">_Value:_</span></span>
  
> <span data-ttu-id="a4750-117">Wertdaten Wert Größe Wertdaten Abstand Wert Größe Wert-IID Wertdaten Textabstand</span><span class="sxs-lookup"><span data-stu-id="a4750-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="a4750-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="a4750-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="a4750-119">Name-Guid Namen Art: Name Name-Id-Guid Namen Art Namen Zeichenfolgenlänge-Zeichenfolge Textabstand</span><span class="sxs-lookup"><span data-stu-id="a4750-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="a4750-120">Die Kapselung jeder Eigenschaft hängt von der Eigenschaftenbezeichner und den Eigenschaftentyp.</span><span class="sxs-lookup"><span data-stu-id="a4750-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="a4750-121">Eigenschaftentags, Bezeichner und Typen werden in den Headerdateien Mapitags.h und Mapidefs.h definiert.</span><span class="sxs-lookup"><span data-stu-id="a4750-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="a4750-122">Wenn die Eigenschaft eine benannte Eigenschaft ist, wird das Eigenschafts-Tag sofort mit dem Namen der MAPI-Eigenschaft, bestehend aus einen global eindeutigen Bezeichner (GUID), einen Typ und eine Kennung oder eine Unicode-Zeichenfolge verfolgt.</span><span class="sxs-lookup"><span data-stu-id="a4750-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="a4750-123">Mehrwertige Eigenschaften und Eigenschaften mit variabler Längenwerte wie die Eigenschaftentypen PT_BINARY, PT_STRING8, PT_UNICODE oder PT_OBJECT werden auf folgende Weise behandelt.</span><span class="sxs-lookup"><span data-stu-id="a4750-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="a4750-124">Zunächst wird die Anzahl der Werte, die als eine lange, nicht signierte 32-Bit-codierte im TNEF-Stream, gefolgt von den einzelnen Werten platziert.</span><span class="sxs-lookup"><span data-stu-id="a4750-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="a4750-125">Jede Eigenschaft Wertdaten ist als die Größe in Byte, gefolgt von der Datenwert selbst codiert.</span><span class="sxs-lookup"><span data-stu-id="a4750-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="a4750-126">Der Datenwert ist 4-Byte-Begrenzung, aufgefüllt Obwohl die den Abstand in die Wert-Größe nicht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a4750-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="a4750-127">Wenn die Eigenschaft vom Typ PT_OBJECT ist, folgt die Wert-Größe der Identifier, der das Objekt.</span><span class="sxs-lookup"><span data-stu-id="a4750-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="a4750-128">Die aktuelle Implementierung von TNEF unterstützt nur die IID_IMessage, IID_IStorage und IID_Istream Schnittstelle-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a4750-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="a4750-129">Die Größe des Bezeichners Schnittstelle ist in die Wert-Größe enthalten.</span><span class="sxs-lookup"><span data-stu-id="a4750-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="a4750-130">Wenn das Objekt eingebettete Nachricht ist (d. h., sie hat einen Eigenschaftentyp PT_OBJECT und eine Schnittstellenbezeichner des IID_Imessage), die Daten des Werts als ein eingebettetes TNEF-Stream codiert.</span><span class="sxs-lookup"><span data-stu-id="a4750-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="a4750-131">Die eigentliche Codierung der eingebettete Nachricht in TNEF-Implementierung erfolgt durch ein zweites TNEF-Objekt für den ursprünglichen Datenstrom öffnen und verarbeiten den Stream Inline.</span><span class="sxs-lookup"><span data-stu-id="a4750-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

