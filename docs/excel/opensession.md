---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e4df0c5772f28ab4ab8d84eaddfe4409a88061b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421837"
---
# <a name="opensession"></a>OpenSession

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Erstellt eine Sitzung, in der benutzerdefinierte Funktionen ausgeführt werden können.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Parameter

_Parameter_
  
> Ein Zeiger auf durch Semikolons getrennte UNICODE-Zeichenfolge von Parametern für die Sitzung. Excel verwendet dieses Argument nicht.
    
## <a name="return-value"></a>Rückgabewert

Eine Sitzungs-ID, die in anderen Aufrufen des Cluster-Konnektors verwendet werden soll, wenn die Sitzung erfolgreich erstellt wurde; andernfalls **xlHpcRetCallFailed**.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

