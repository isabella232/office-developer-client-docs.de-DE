---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e7b3774d8dce446f0e87f041f11dac607f464680
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795725"
---
# <a name="tchar"></a>TCHAR

  
  
**Betrifft**: Outlook 
  
Eine Win32-Zeichenfolge, die verwendet werden kann, um ANSI-, DBCS- oder Unicode-Zeichenfolgen zu beschreiben. F�r ANSI- und DBCS-Plattformen wird TCHAR wie folgt definiert:
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a>Hinweise

F�r Unicode-Plattformen wird TCHAR als Synonym f�r den Typ WCHAR definiert. 
  
MAPI-Clients k�nnen den Datentyp TCHAR verwenden, um eine Zeichenfolge des Typs WCHAR oder Char darzustellen. Achten Sie darauf, den symbolischen Konstanten-UNICODE zu definieren und die Plattform einzuschr�nken, wenn dies erforderlich ist. MAPI interpretiert die Plattforminformationen �bersetzt TCHAR intern in die entsprechende Zeichenfolge. Der MAPI-Eigenschaftentyp, PT_TSTRING, funktioniert genauso wie der TCHAR-Datentyp. Wenn die Plattform Unicode unterst�tzt, werden die Eigenschaften vom Typ PT_TSTRING bei der Kompilierung dem Typ PT_UNICODE zugewiesen. Wenn die Plattform Unicode nicht unterst�tzt, werden diese Eigenschaften dem Typ PT_STRING8 zugewiesen.
  
Weitere Informationen �ber diese Funktionen finden Sie unter [Zeichens�tzen](mapi-character-sets.md) und [Liste der Eigenschaftstypen](property-types.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Datentypen](mapi-data-types.md)

