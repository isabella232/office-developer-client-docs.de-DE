---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b3fefaa2308a07e73e946910feb58f58b67d54c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631097"
---
# <a name="attmapiprops"></a>attMAPIProps

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **Attribut "attMAPIProps"** ist dadurch besonders, dass es verwendet werden kann, um jede MAPI-Eigenschaft zu codieren, die kein Gegenstück in der Gruppe vorhandener TNEF-definierter Attribute aufweist. Bei den Attributdaten handelt es sich um eine Gezählte von MAPI-Eigenschaften, die end-to-end angeordnet sind. Das Format dieser Codierung, die einen beliebigen Satz von MAPI-Eigenschaften zulässt, lautet wie folgt:  
  
 _Property_Seq:_
  
> eigenschaftsanzahl  _Property_Value,..._
    
Es müssen so viele  _Property_Value_ Elemente vorhanden sein, wie der Wert für die Eigenschaftsanzahl angibt. 
  
 _Property_Value:_
  
> property-tag _Property_property-tag  _Proptag_Name Property_
    
Das Eigenschaftstag ist einfach der Wert, der dem Eigenschaftenbezeichner zugeordnet ist, z. B. 0x0037001F für **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).
  
 _Eigenschaft:_
  
>   Wert-Anzahl-Wert,... 
    
 _Wert:_
  
> Wert-Daten-Wert-Größe-Wert-Datenabstand Wert-Größe-IID-Wert-Datenabstand
    
 _Proptag_Name:_
  
> name-guid name-kind name-id name-guid name-kind name-string-length name-string padding
    
Die Kapselung der einzelnen Eigenschaften variiert je nach Eigenschaftsbezeichner und Eigenschaftstyp. Eigenschaftstags, Bezeichner und Typen werden in den Headerdateien Mapitags.h und Mapidefs.h definiert.
  
Wenn es sich bei der Eigenschaft um eine benannte Eigenschaft handelt, folgt unmittelbar auf das Eigenschaftentag der MAPI-Eigenschaftsname, der aus einer GUID (Globally Unique Identifier), einem Typ und einem Bezeichner oder einer Unicode-Zeichenfolge besteht.
  
Mehrwertige Eigenschaften und Eigenschaften mit Werten variabler Länge, z. B. die Eigenschaftentypen PT_BINARY, PT_STRING8, PT_UNICODE oder PT_OBJECT, werden wie folgt behandelt. Zuerst wird die Anzahl der Werte, die als 32-Bit-Länge ohne Vorzeichen codiert sind, im TNEF-Datenstrom platziert, gefolgt von den einzelnen Werten. Die Wertdaten jeder Eigenschaft werden als Größe in Byte codiert, gefolgt von den Wertdaten selbst. Die Wertdaten werden auf eine 4-Byte-Grenze aufgefüllt, obwohl die Abstandsmenge nicht in der Wertgröße enthalten ist.
  
Wenn die Eigenschaft vom Typ PT_OBJECT ist, folgt auf die Wertgröße der Schnittstellenbezeichner des Objekts. Die aktuelle Implementierung von TNEF unterstützt nur die IID_IMessage-, IID_IStorage- und IID_Istream-Schnittstellenbezeichner. Die Größe des Schnittstellenbezeichners ist in der Wertgröße enthalten.
  
Wenn es sich bei dem Objekt um eine eingebettete Nachricht handelt (d. h. es verfügt über einen Eigenschaftentyp von PT_OBJECT und einen Schnittstellenbezeichner von IID_Imessage), werden die Wertdaten als eingebetteter TNEF-Datenstrom codiert. Die tatsächliche Codierung einer eingebetteten Nachricht in der TNEF-Implementierung erfolgt, indem ein zweites TNEF-Objekt für den ursprünglichen Datenstrom geöffnet und der Datenstrom inline verarbeitet wird.
  

