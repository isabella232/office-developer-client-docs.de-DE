---
title: attDate-Attribute
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f3319c9ae49fa97a6179b0ee800bd5dd594aefab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791333"
---
# <a name="attdate-attributes"></a>attDate-Attribute

  
  
**Betrifft**: Outlook 
  
Alle MAPI-Eigenschaften, die sich auf die Datums- und Zeitangaben beziehen sind TNEF-Attributen zugeordnet, die das Präfix **AttDate** aufweisen. Diese werden alle als **DTR** Strukturen codiert. Die Datums- und Zeitangaben für Anlagenattribute werden als auch Strukturen **DTR** codiert. 
  
Alle MAPI-Eigenschaften, die sich auf die Datums- und Zeitangaben beziehen sind TNEF-Attributen zugeordnet, die das Präfix **AttDate** aufweisen. Diese werden alle als **DTR** Strukturen codiert. Die Datums- und Zeitangaben für Anlagenattribute werden als auch Strukturen **DTR** codiert. 
  
Eine Struktur **DTR** ähnelt der **SYSTEMTIME** -Struktur, die in den Win32-Headerdateien definiert. Die Struktur **DTR** wird als **sizeof(DTR)** Bytes, beginnend mit dem ersten Element der Struktur in der TNEF-Stream codiert. Die **DTR** -Struktur ist in der TNEF definiert. H-Headerdatei. 
  

