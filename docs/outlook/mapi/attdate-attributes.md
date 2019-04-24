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
ms.openlocfilehash: b7c1ce8d0338a2bda63a276628bdd6e8be3b8eb1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318067"
---
# <a name="attdate-attributes"></a>attDate-Attribute

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle MAPI-Eigenschaften, die sich auf Datums-und Uhrzeitangaben beziehen, werden TNEF-Attributen zugeordnet, die das **attDate** -Präfix aufweisen. Diese sind alle als **DTR** -Strukturen codiert. Die Datums-und Uhrzeitangaben für Anlagenattribute werden ebenfalls als **DTR** -Strukturen codiert. 
  
Alle MAPI-Eigenschaften, die sich auf Datums-und Uhrzeitangaben beziehen, werden TNEF-Attributen zugeordnet, die das **attDate** -Präfix aufweisen. Diese sind alle als **DTR** -Strukturen codiert. Die Datums-und Uhrzeitangaben für Anlagenattribute werden ebenfalls als **DTR** -Strukturen codiert. 
  
Eine **DTR** -Struktur ähnelt der in den Win32-Headerdateien definierten **System** Zeitstruktur. Die **DTR** -Struktur wird im TNEF-Stream als **sizeof (DTR)-** Byte, beginnend mit dem ersten Element der Struktur, codiert. Die **DTR** -Struktur ist im TNEF definiert. H-Headerdatei. 
  

