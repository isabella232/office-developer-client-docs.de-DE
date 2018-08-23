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
# <a name="tchar"></a><span data-ttu-id="3d5b2-103">TCHAR</span><span class="sxs-lookup"><span data-stu-id="3d5b2-103">TCHAR</span></span>

  
  
<span data-ttu-id="3d5b2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d5b2-104">**Applies to**: Office 365 | Outlook | Outlook 2016</span></span> 
  
<span data-ttu-id="3d5b2-p101">Eine Win32-Zeichenfolge, die verwendet werden kann, um ANSI-, DBCS- oder Unicode-Zeichenfolgen zu beschreiben. Für ANSI- und DBCS-Plattformen wird TCHAR wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="3d5b2-p101">A Win32 character string that can be used to describe ANSI, DBCS, or Unicode strings. For ANSI and DBCS platforms, TCHAR is defined as follows:</span></span>
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a><span data-ttu-id="3d5b2-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d5b2-107">Remarks</span></span>

<span data-ttu-id="3d5b2-108">Für Unicode-Plattformen wird TCHAR als Synonym für den Typ WCHAR definiert.</span><span class="sxs-lookup"><span data-stu-id="3d5b2-108">For Unicode platforms, TCHAR is defined as synonymous with the WCHAR type.</span></span> 
  
<span data-ttu-id="3d5b2-p102">MAPI-Clients können den Datentyp TCHAR verwenden, um eine Zeichenfolge des Typs WCHAR oder Char darzustellen. Achten Sie darauf, den symbolischen Konstanten-UNICODE zu definieren und die Plattform einzuschränken, wenn dies erforderlich ist. MAPI interpretiert die Plattforminformationen übersetzt TCHAR intern in die entsprechende Zeichenfolge. Der MAPI-Eigenschaftentyp, PT_TSTRING, funktioniert genauso wie der TCHAR-Datentyp. Wenn die Plattform Unicode unterstützt, werden die Eigenschaften vom Typ PT_TSTRING bei der Kompilierung dem Typ PT_UNICODE zugewiesen. Wenn die Plattform Unicode nicht unterstützt, werden diese Eigenschaften dem Typ PT_STRING8 zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3d5b2-p102">MAPI clients can use the TCHAR data type to represent a string of either the WCHAR or char type. Be sure to define the symbolic constant UNICODE and limit the platform when it is required. MAPI will interpret the platform information and internally translate TCHAR to the appropriate string. The MAPI property type, PT_TSTRING, works just like the TCHAR data type. When the platform supports Unicode, properties of type PT_TSTRING are assigned the type PT_UNICODE at compile time. When the platform does not support Unicode, these properties are assigned the type PT_STRING8.</span></span>
  
<span data-ttu-id="3d5b2-115">Weitere Informationen über diese Funktionen finden Sie unter [Zeichensätzen](mapi-character-sets.md) und [Liste der Eigenschaftstypen](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="3d5b2-115">For more information about this functionality, see [Character Sets](mapi-character-sets.md) and [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d5b2-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d5b2-116">See also</span></span>



[<span data-ttu-id="3d5b2-117">MAPI-Datentypen</span><span class="sxs-lookup"><span data-stu-id="3d5b2-117">MAPI Data Types</span></span>](mapi-data-types.md)

