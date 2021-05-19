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
# <a name="attmapiprops"></a>attMAPIProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **attMAPIProps-Attribut** ist besonders, da es zum Codieren einer beliebigen MAPI-Eigenschaft verwendet werden kann, die kein Gegenstück im Satz vorhandener TNEF-definierter Attribute hat. Bei den Attributdaten handelt es sich um einen gezählten Satz von MAPI-Eigenschaften, die ende-zu-Ende gelegt werden. Das Format dieser Codierung, das einen beliebigen Satz von MAPI-Eigenschaften zulässt, lautet wie folgt:  
  
 _Property_Seq:_
  
> Eigenschaftsanzahl  _Property_Value,..._
    
Es muss so viele  _Property_Value_ wie der Eigenschaftsanzahlswert angibt. 
  
 _Property_Value:_
  
> property-tag _Property_property-tag  _Proptag_Name Property_
    
Das Property-Tag ist einfach der Wert, der dem Eigenschaftenbezeichner zugeordnet ist, z. B. 0x0037001F für **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Eigenschaft:_
  
>  _Value-Count_  _Value,..._
    
 _Wert:_
  
> value-data value-size value-data padding value-size value-IID value-data padding
    
 _Proptag_Name:_
  
> name-guid name-kind name-id name-guid name-kind name-string-length name-string padding
    
Die Kapselung der einzelnen Eigenschaften variiert je nach Eigenschafts-ID und Eigenschaftstyp. Eigenschaftstags, Bezeichner und Typen werden in den Headerdateien Mapitags.h und Mapidefs.h definiert.
  
Wenn es sich bei der Eigenschaft um eine benannte Eigenschaft handelt, folgt dem Eigenschaftstag sofort der Name der MAPI-Eigenschaft, der aus einer guiD (Globally Unique Identifier), einem Typ und einem Bezeichner oder einer Unicode-Zeichenfolge besteht.
  
Mehrwertige Eigenschaften und Eigenschaften mit Variablenlängenwerten, z. B. PT_BINARY-, PT_STRING8-, PT_UNICODE- oder PT_OBJECT-Eigenschaftstypen, werden wie folgt behandelt. Zunächst wird die Anzahl der Werte, die als 32-Bit-Long-Wert ohne Vorzeichen codiert sind, im TNEF-Stream platziert, gefolgt von den einzelnen Werten. Die Wertdaten jeder Eigenschaft werden als Größe in Bytes codiert, gefolgt von den Wertdaten selbst. Die Wertdaten werden auf eine 4-Byte-Grenze gepolstert, obwohl der Abstand nicht in der Größengröße enthalten ist.
  
Wenn die Eigenschaft vom Typ PT_OBJECT, folgt auf die Wertgröße der Schnittstellenbezeichner des Objekts. Die aktuelle Implementierung von TNEF unterstützt nur die IID_IMessage, IID_IStorage und IID_Istream Schnittstellenbezeichner. Die Größe der Schnittstellen-ID ist in der Wertgröße enthalten.
  
Wenn es sich bei dem Objekt um eine eingebettete Nachricht handelt (d. h. es hat den Eigenschaftstyp PT_OBJECT und einen Schnittstellenbezeichner von IID_Imessage), werden die Wertdaten als eingebetteter TNEF-Stream codiert. Die tatsächliche Codierung einer eingebetteten Nachricht in der TNEF-Implementierung erfolgt durch Öffnen eines zweiten TNEF-Objekts für den ursprünglichen Datenstrom und Verarbeiten des Datenstroms inline.
  

