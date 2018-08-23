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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 357ace3267f22d751a20a12c96f108ee2f8ae1e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595202"
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

