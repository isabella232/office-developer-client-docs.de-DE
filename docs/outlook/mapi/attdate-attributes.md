---
title: attDate-Attribute
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22801641-752c-4c81-be90-02039eaa4277
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ff0cc6b1c17b2ed83d7b0ec0921904763da8624b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567013"
---
# <a name="attdate-attributes"></a>attDate-Attribute

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Alle MAPI-Eigenschaften, die sich auf die Datums- und Zeitangaben beziehen sind TNEF-Attributen zugeordnet, die das Präfix **AttDate** aufweisen. Diese werden alle als **DTR** Strukturen codiert. Die Datums- und Zeitangaben für Anlagenattribute werden als auch Strukturen **DTR** codiert. 
  
Alle MAPI-Eigenschaften, die sich auf die Datums- und Zeitangaben beziehen sind TNEF-Attributen zugeordnet, die das Präfix **AttDate** aufweisen. Diese werden alle als **DTR** Strukturen codiert. Die Datums- und Zeitangaben für Anlagenattribute werden als auch Strukturen **DTR** codiert. 
  
Eine Struktur **DTR** ähnelt der **SYSTEMTIME** -Struktur, die in den Win32-Headerdateien definiert. Die Struktur **DTR** wird als **sizeof(DTR)** Bytes, beginnend mit dem ersten Element der Struktur in der TNEF-Stream codiert. Die **DTR** -Struktur ist in der TNEF definiert. H-Headerdatei. 
  

