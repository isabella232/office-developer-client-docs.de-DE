---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eef480e8b024565ab282fb242a36336cd17384a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791329"
---
# <a name="attmapiprops"></a>attMAPIProps

  
  
**Betrifft**: Outlook 
  
Das Attribut **AttMAPIProps** werden spezielle zum Codieren von MAPI-Eigenschaften, die kein Gegenstück in der Gruppe von vorhandenen TNEF benutzerdefinierte Attribute verwendet werden können. Die Attributdaten ist ein gezählte festgelegten End-to-End-MAPI-Eigenschaften. Das Format dieser Codierung, die für jeden Satz von MAPI-Eigenschaften werden kann, ist wie folgt:  
  
 _Property_Seq:_
  
> Eigenschaft Count _Property_Value..._
    
Gibt an, der Wert der Eigenschaft Count _Property_Value_ Elemente muss vorhanden sein. 
  
 _Property_Value:_
  
> Eigenschafts-Tag _Property_property-Tag _Proptag_Name-Eigenschaft_
    
Das Eigenschaft-Tag ist einfach den Wert der Eigenschaft-ID, wie etwa 0x0037001F für **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) zugeordnet.
  
 _Eigenschaft:_
  
>  _Wert_ Wert-Count _Value..._
    
 _Wert:_
  
> Wertdaten Wert Größe Wertdaten Abstand Wert Größe Wert-IID Wertdaten Textabstand
    
 _Proptag_Name:_
  
> Name-Guid Namen Art: Name Name-Id-Guid Namen Art Namen Zeichenfolgenlänge-Zeichenfolge Textabstand
    
Die Kapselung jeder Eigenschaft hängt von der Eigenschaftenbezeichner und den Eigenschaftentyp. Eigenschaftentags, Bezeichner und Typen werden in den Headerdateien Mapitags.h und Mapidefs.h definiert.
  
Wenn die Eigenschaft eine benannte Eigenschaft ist, wird das Eigenschafts-Tag sofort mit dem Namen der MAPI-Eigenschaft, bestehend aus einen global eindeutigen Bezeichner (GUID), einen Typ und eine Kennung oder eine Unicode-Zeichenfolge verfolgt.
  
Mehrwertige Eigenschaften und Eigenschaften mit variabler Längenwerte wie die Eigenschaftentypen PT_BINARY, PT_STRING8, PT_UNICODE oder PT_OBJECT werden auf folgende Weise behandelt. Zunächst wird die Anzahl der Werte, die als eine lange, nicht signierte 32-Bit-codierte im TNEF-Stream, gefolgt von den einzelnen Werten platziert. Jede Eigenschaft Wertdaten ist als die Größe in Byte, gefolgt von der Datenwert selbst codiert. Der Datenwert ist 4-Byte-Begrenzung, aufgefüllt Obwohl die den Abstand in die Wert-Größe nicht enthalten ist.
  
Wenn die Eigenschaft vom Typ PT_OBJECT ist, folgt die Wert-Größe der Identifier, der das Objekt. Die aktuelle Implementierung von TNEF unterstützt nur die IID_IMessage, IID_IStorage und IID_Istream Schnittstelle-Bezeichner. Die Größe des Bezeichners Schnittstelle ist in die Wert-Größe enthalten.
  
Wenn das Objekt eingebettete Nachricht ist (d. h., sie hat einen Eigenschaftentyp PT_OBJECT und eine Schnittstellenbezeichner des IID_Imessage), die Daten des Werts als ein eingebettetes TNEF-Stream codiert. Die eigentliche Codierung der eingebettete Nachricht in TNEF-Implementierung erfolgt durch ein zweites TNEF-Objekt für den ursprünglichen Datenstrom öffnen und verarbeiten den Stream Inline.
  

