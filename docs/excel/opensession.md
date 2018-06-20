---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 782843f11643e203488b313181d224443a1d36c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790561"
---
# <a name="opensession"></a>OpenSession

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Erstellt eine Sitzung in der benutzerdefinierten Funktionen ausgeführt werden können.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Parameter

_Params_
  
> Ein Zeiger auf die durch Semikolons getrennte Unicode-Zeichenfolge der Parameter für die Sitzung. Excel wird dieses Argument nicht verwendet.
    
## <a name="return-value"></a>R�ckgabewert

Eine ID für eine Sitzung in anderen Aufrufe an den Konnektor Cluster verwenden, wenn die Sitzung erfolgreich erstellt wurde; andernfalls **XlHpcRetCallFailed**.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

