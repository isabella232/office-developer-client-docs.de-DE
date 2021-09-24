---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.localizationpriority: high
ms.openlocfilehash: 86eef598a84ed7cd11d1fdcc6350375c6421a029
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549875"
---
# <a name="tchar"></a>TCHAR

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Win32-Zeichenfolge, die verwendet werden kann, um ANSI-, DBCS- oder Unicode-Zeichenfolgen zu beschreiben. Für ANSI- und DBCS-Plattformen wird TCHAR wie folgt definiert:
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a>Bemerkungen

Für Unicode-Plattformen wird TCHAR als Synonym für den Typ WCHAR definiert. 
  
MAPI-Clients können den Datentyp TCHAR verwenden, um eine Zeichenfolge des Typs WCHAR oder Char darzustellen. Achten Sie darauf, den symbolischen Konstanten-UNICODE zu definieren und die Plattform einzuschränken, wenn dies erforderlich ist. MAPI interpretiert die Plattforminformationen übersetzt TCHAR intern in die entsprechende Zeichenfolge. Der MAPI-Eigenschaftentyp, PT_TSTRING, funktioniert genauso wie der TCHAR-Datentyp. Wenn die Plattform Unicode unterstützt, werden die Eigenschaften vom Typ PT_TSTRING bei der Kompilierung dem Typ PT_UNICODE zugewiesen. Wenn die Plattform Unicode nicht unterstützt, werden diese Eigenschaften dem Typ PT_STRING8 zugewiesen.
  
Weitere Informationen über diese Funktionen finden Sie unter [Zeichensätzen](mapi-character-sets.md) und [Liste der Eigenschaftstypen](property-types.md). 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Datentypen](mapi-data-types.md)

