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
ms.openlocfilehash: 185bfbb151c4f8d4e36b40b94393d14d50c33edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410455"
---
# <a name="attmapiprops"></a><span data-ttu-id="c071a-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="c071a-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="c071a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c071a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c071a-105">Das **attMAPIProps** -Attribut ist insofern besonders, als dass es verwendet werden kann, um jede MAPI-Eigenschaft zu codieren, die kein Gegenstück zu den vorhandenen TNEF-definierten Attributen hat.</span><span class="sxs-lookup"><span data-stu-id="c071a-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="c071a-106">Die Attributdaten sind ein gezählter Satz von MAPI-Eigenschaften, die End-to-End festgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="c071a-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="c071a-107">Das Format dieser Codierung, das eine beliebige Gruppe von MAPI-Eigenschaften zulässt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c071a-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="c071a-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="c071a-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="c071a-109">Eigenschaft-Count _Property_Value,..._</span><span class="sxs-lookup"><span data-stu-id="c071a-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="c071a-110">Es muss so viele _Property_Value_ -Elemente geben, wie der Wert der Eigenschafts Anzahl angibt.</span><span class="sxs-lookup"><span data-stu-id="c071a-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="c071a-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="c071a-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="c071a-112">Property-Tag _Property_property- _Proptag_Name-Eigenschaft_</span><span class="sxs-lookup"><span data-stu-id="c071a-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="c071a-113">Das Property-Tag ist einfach der Wert, der dem Eigenschaftenbezeichner zugeordnet ist, beispielsweise 0x0037001F für **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c071a-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="c071a-114">_Eigenschaft_</span><span class="sxs-lookup"><span data-stu-id="c071a-114">_Property:_</span></span>
  
>  <span data-ttu-id="c071a-115">__ Value-count-Wert _,..._</span><span class="sxs-lookup"><span data-stu-id="c071a-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="c071a-116">_Wert:_</span><span class="sxs-lookup"><span data-stu-id="c071a-116">_Value:_</span></span>
  
> <span data-ttu-id="c071a-117">Wert-Data Value-size value-Data Padding Value-size value-IID Value-Data Padding</span><span class="sxs-lookup"><span data-stu-id="c071a-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="c071a-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="c071a-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="c071a-119">Name-GUID-Name-kindname-ID Name-GUID Name-Art Name-String-length Name-String Padding</span><span class="sxs-lookup"><span data-stu-id="c071a-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="c071a-120">Die Kapselung der einzelnen Eigenschaften variiert basierend auf dem Eigenschaftenbezeichner und dem Eigenschaftentyp.</span><span class="sxs-lookup"><span data-stu-id="c071a-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="c071a-121">Eigenschaftentags, Bezeichner und Typen werden in den Headerdateien Mapitags. h und Mapidefs. h definiert.</span><span class="sxs-lookup"><span data-stu-id="c071a-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="c071a-122">Wenn es sich bei der Eigenschaft um eine benannte Eigenschaft handelt, folgt sofort der MAPI-Eigenschaften Name, bestehend aus einem global eindeutigen Bezeichner (GUID), einem Typ und einem Bezeichner oder einer Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c071a-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="c071a-123">Mehrwertige Eigenschaften und Eigenschaften mit Variablen Längenwerten wie den PT_BINARY-, PT_STRING8-, PT_UNICODE-oder PT_OBJECT-Eigenschaftstypen werden folgendermaßen behandelt.</span><span class="sxs-lookup"><span data-stu-id="c071a-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="c071a-124">Zuerst wird die Anzahl der Werte, die als 32-Bit unsigned long codiert wurden, im TNEF-Stream, gefolgt von den einzelnen Werten, angegeben.</span><span class="sxs-lookup"><span data-stu-id="c071a-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="c071a-125">Die Wert Daten der einzelnen Eigenschaften werden als Größe in Bytes codiert, gefolgt von den Wert Daten selbst.</span><span class="sxs-lookup"><span data-stu-id="c071a-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="c071a-126">Die Wertdaten werden zu einer 4-Byte-Grenze aufgefüllt, obwohl die Menge an Abstand nicht in der Wertgröße enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c071a-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="c071a-127">Wenn die Eigenschaft vom Typ PT_OBJECT ist, folgt die Wertgröße dem Schnittstellenbezeichner des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c071a-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="c071a-128">Die aktuelle Implementierung von TNEF unterstützt nur die IID_IMessage-, IID_IStorage-und IID_Istream-Schnittstellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="c071a-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="c071a-129">Die Größe des Schnittstellen Bezeichners ist in der Wertgröße enthalten.</span><span class="sxs-lookup"><span data-stu-id="c071a-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="c071a-130">Wenn es sich bei dem Objekt um eine eingebettete Nachricht handelt (also einen Eigenschaftentyp von PT_OBJECT und einen Schnittstellenbezeichner von IID_Imessage), werden die Wertdaten als eingebetteter TNEF-Stream codiert.</span><span class="sxs-lookup"><span data-stu-id="c071a-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="c071a-131">Die tatsächliche Codierung einer eingebetteten Nachricht in der TNEF-Implementierung erfolgt durch Öffnen eines zweiten TNEF-Objekts für den ursprünglichen Stream und Inline Verarbeitung des Streams.</span><span class="sxs-lookup"><span data-stu-id="c071a-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

