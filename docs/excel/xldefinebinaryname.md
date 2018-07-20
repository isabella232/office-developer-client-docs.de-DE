---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- XlDefineBinaryName-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790585"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="2ff06-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="2ff06-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="2ff06-105">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2ff06-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2ff06-106">Verwendet, um ein beständiger Speicher für eine **XltypeBigData** **XLOPER**verteilen/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="2ff06-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="2ff06-107">Mit einem definierten Namen für die binäre Daten werden mit der Arbeitsmappe gespeichert und namentlich jederzeit zugegriffen werden können.</span><span class="sxs-lookup"><span data-stu-id="2ff06-107">Data with a defined binary name is saved with the workbook, and can be accessed by name at any time.</span></span> <span data-ttu-id="2ff06-108">Weitere Informationen finden Sie unter "Binary Namen Bereich Einschränkung" unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="2ff06-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="2ff06-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ff06-109">Parameters</span></span>

 <span data-ttu-id="2ff06-110">_pxName_ (**XltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="2ff06-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="2ff06-111">Eine Zeichenfolge zur Angabe der Name der Daten.</span><span class="sxs-lookup"><span data-stu-id="2ff06-111">A string specifying the name of the data.</span></span> <span data-ttu-id="2ff06-112">Die Zeichenfolge ist, gelten die gleichen Einschränkungen wie definierte Namen benennen.</span><span class="sxs-lookup"><span data-stu-id="2ff06-112">The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="2ff06-113">_pxData_ (**XltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="2ff06-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="2ff06-114">Bigdata-Struktur, die die zu speichernden Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="2ff06-114">Bigdata structure specifying the data to be stored.</span></span> <span data-ttu-id="2ff06-115">Wenn Sie diese Funktion aufrufen, sollte das **LpbData** Mitglied der **Bigdata** -Struktur zeigen Sie auf die Daten für die der Namen definiert wird, und der **CbData** Member sollte die Länge der Daten in Bytes enthalten.</span><span class="sxs-lookup"><span data-stu-id="2ff06-115">When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="2ff06-116">Wenn das Argument _PxData_ nicht angegebenen (**XltypeMissing**) ist, wird die benannte Zuweisung von _PxName_ angegebenen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2ff06-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2ff06-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ff06-117">See also</span></span>



[<span data-ttu-id="2ff06-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="2ff06-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="2ff06-119">C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können</span><span class="sxs-lookup"><span data-stu-id="2ff06-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="2ff06-120">Bekannte Probleme in Excel XLL-Entwicklung</span><span class="sxs-lookup"><span data-stu-id="2ff06-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

