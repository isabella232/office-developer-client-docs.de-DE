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
# <a name="attmapiprops"></a><span data-ttu-id="6f77c-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="6f77c-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="6f77c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f77c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f77c-105">Das **attMAPIProps-Attribut** ist besonders, da es zum Codieren einer beliebigen MAPI-Eigenschaft verwendet werden kann, die kein Gegenstück im Satz vorhandener TNEF-definierter Attribute hat.</span><span class="sxs-lookup"><span data-stu-id="6f77c-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="6f77c-106">Bei den Attributdaten handelt es sich um einen gezählten Satz von MAPI-Eigenschaften, die ende-zu-Ende gelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6f77c-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="6f77c-107">Das Format dieser Codierung, das einen beliebigen Satz von MAPI-Eigenschaften zulässt, lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="6f77c-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="6f77c-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="6f77c-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="6f77c-109">Eigenschaftsanzahl  _Property_Value,..._</span><span class="sxs-lookup"><span data-stu-id="6f77c-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="6f77c-110">Es muss so viele  _Property_Value_ wie der Eigenschaftsanzahlswert angibt.</span><span class="sxs-lookup"><span data-stu-id="6f77c-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="6f77c-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="6f77c-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="6f77c-112">property-tag _Property_property-tag  _Proptag_Name Property_</span><span class="sxs-lookup"><span data-stu-id="6f77c-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="6f77c-113">Das Property-Tag ist einfach der Wert, der dem Eigenschaftenbezeichner zugeordnet ist, z. B. 0x0037001F für **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6f77c-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="6f77c-114">_Eigenschaft:_</span><span class="sxs-lookup"><span data-stu-id="6f77c-114">_Property:_</span></span>
  
>  <span data-ttu-id="6f77c-115">_Value-Count_  _Value,..._</span><span class="sxs-lookup"><span data-stu-id="6f77c-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="6f77c-116">_Wert:_</span><span class="sxs-lookup"><span data-stu-id="6f77c-116">_Value:_</span></span>
  
> <span data-ttu-id="6f77c-117">value-data value-size value-data padding value-size value-IID value-data padding</span><span class="sxs-lookup"><span data-stu-id="6f77c-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="6f77c-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="6f77c-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="6f77c-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span><span class="sxs-lookup"><span data-stu-id="6f77c-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="6f77c-120">Die Kapselung der einzelnen Eigenschaften variiert je nach Eigenschafts-ID und Eigenschaftstyp.</span><span class="sxs-lookup"><span data-stu-id="6f77c-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="6f77c-121">Eigenschaftstags, Bezeichner und Typen werden in den Headerdateien Mapitags.h und Mapidefs.h definiert.</span><span class="sxs-lookup"><span data-stu-id="6f77c-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="6f77c-122">Wenn es sich bei der Eigenschaft um eine benannte Eigenschaft handelt, folgt dem Eigenschaftstag sofort der Name der MAPI-Eigenschaft, der aus einer guiD (Globally Unique Identifier), einem Typ und einem Bezeichner oder einer Unicode-Zeichenfolge besteht.</span><span class="sxs-lookup"><span data-stu-id="6f77c-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="6f77c-123">Mehrwertige Eigenschaften und Eigenschaften mit Variablenlängenwerten, z. B. PT_BINARY-, PT_STRING8-, PT_UNICODE- oder PT_OBJECT-Eigenschaftstypen, werden wie folgt behandelt.</span><span class="sxs-lookup"><span data-stu-id="6f77c-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="6f77c-124">Zunächst wird die Anzahl der Werte, die als 32-Bit-Long-Wert ohne Vorzeichen codiert sind, im TNEF-Stream platziert, gefolgt von den einzelnen Werten.</span><span class="sxs-lookup"><span data-stu-id="6f77c-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="6f77c-125">Die Wertdaten jeder Eigenschaft werden als Größe in Bytes codiert, gefolgt von den Wertdaten selbst.</span><span class="sxs-lookup"><span data-stu-id="6f77c-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="6f77c-126">Die Wertdaten werden auf eine 4-Byte-Grenze gepolstert, obwohl der Abstand nicht in der Größengröße enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6f77c-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="6f77c-127">Wenn die Eigenschaft vom Typ PT_OBJECT, folgt auf die Wertgröße der Schnittstellenbezeichner des Objekts.</span><span class="sxs-lookup"><span data-stu-id="6f77c-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="6f77c-128">Die aktuelle Implementierung von TNEF unterstützt nur die IID_IMessage, IID_IStorage und IID_Istream Schnittstellenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="6f77c-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="6f77c-129">Die Größe der Schnittstellen-ID ist in der Wertgröße enthalten.</span><span class="sxs-lookup"><span data-stu-id="6f77c-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="6f77c-130">Wenn es sich bei dem Objekt um eine eingebettete Nachricht handelt (d. h. es hat den Eigenschaftstyp PT_OBJECT und einen Schnittstellenbezeichner von IID_Imessage), werden die Wertdaten als eingebetteter TNEF-Stream codiert.</span><span class="sxs-lookup"><span data-stu-id="6f77c-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="6f77c-131">Die tatsächliche Codierung einer eingebetteten Nachricht in der TNEF-Implementierung erfolgt durch Öffnen eines zweiten TNEF-Objekts für den ursprünglichen Datenstrom und Verarbeiten des Datenstroms inline.</span><span class="sxs-lookup"><span data-stu-id="6f77c-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

