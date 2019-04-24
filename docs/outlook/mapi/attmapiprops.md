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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318123"
---
# <a name="attmapiprops"></a>attMAPIProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **attMAPIProps** -Attribut ist insofern besonders, als dass es verwendet werden kann, um jede MAPI-Eigenschaft zu codieren, die kein Gegenstück zu den vorhandenen TNEF-definierten Attributen hat. Die Attributdaten sind ein gezählter Satz von MAPI-Eigenschaften, die End-to-End festgelegt wurden. Das Format dieser Codierung, das eine beliebige Gruppe von MAPI-Eigenschaften zulässt, lautet wie folgt:  
  
 _Property_Seq:_
  
> Eigenschaft-Count _Property_Value,..._
    
Es muss so viele _Property_Value_ -Elemente geben, wie der Wert der Eigenschafts Anzahl angibt. 
  
 _Property_Value:_
  
> Property-Tag _Property_property- _Proptag_Name-Eigenschaft_
    
Das Property-Tag ist einfach der Wert, der dem Eigenschaftenbezeichner zugeordnet ist, beispielsweise 0x0037001F für **PR_Subject** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Eigenschaft_
  
>  __ Value-count-Wert _,..._
    
 _Wert:_
  
> Wert-Data Value-size value-Data Padding Value-size value-IID Value-Data Padding
    
 _Proptag_Name:_
  
> Name-GUID-Name-kindname-ID Name-GUID Name-Art Name-String-length Name-String Padding
    
Die Kapselung der einzelnen Eigenschaften variiert basierend auf dem Eigenschaftenbezeichner und dem Eigenschaftentyp. Eigenschaftentags, Bezeichner und Typen werden in den Headerdateien Mapitags. h und Mapidefs. h definiert.
  
Wenn es sich bei der Eigenschaft um eine benannte Eigenschaft handelt, folgt sofort der MAPI-Eigenschaften Name, bestehend aus einem global eindeutigen Bezeichner (GUID), einem Typ und einem Bezeichner oder einer Unicode-Zeichenfolge.
  
Mehrwertige Eigenschaften und Eigenschaften mit Variablen Längenwerten wie den PT_BINARY-, PT_STRING8-, PT_UNICODE-oder PT_OBJECT-Eigenschaftstypen werden folgendermaßen behandelt. Zuerst wird die Anzahl der Werte, die als 32-Bit unsigned long codiert wurden, im TNEF-Stream, gefolgt von den einzelnen Werten, angegeben. Die Wert Daten der einzelnen Eigenschaften werden als Größe in Bytes codiert, gefolgt von den Wert Daten selbst. Die Wertdaten werden zu einer 4-Byte-Grenze aufgefüllt, obwohl die Menge an Abstand nicht in der Wertgröße enthalten ist.
  
Wenn die Eigenschaft vom Typ PT_OBJECT ist, folgt die Wertgröße dem Schnittstellenbezeichner des Objekts. Die aktuelle Implementierung von TNEF unterstützt nur die IID_IMessage-, IID_IStorage-und IID_Istream-Schnittstellenbezeichner. Die Größe des Schnittstellen Bezeichners ist in der Wertgröße enthalten.
  
Wenn es sich bei dem Objekt um eine eingebettete Nachricht handelt (also einen Eigenschaftentyp von PT_OBJECT und einen Schnittstellenbezeichner von IID_Imessage), werden die Wertdaten als eingebetteter TNEF-Stream codiert. Die tatsächliche Codierung einer eingebetteten Nachricht in der TNEF-Implementierung erfolgt durch Öffnen eines zweiten TNEF-Objekts für den ursprünglichen Stream und Inline Verarbeitung des Streams.
  

