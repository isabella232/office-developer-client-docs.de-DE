---
title: OpenSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6cfd3513-800f-4602-b3e6-6430920718d6
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a9103430bf340837f22302d5ba76adcb197e8fdb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631496"
---
# <a name="opensession"></a>OpenSession

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Erstellt eine Sitzung, in der benutzerdefinierte Funktionen ausgeführt werden können.
  
```cpp
int OpenSession(WCHAR *Params)
```

## <a name="parameters"></a>Parameter

_Parameter_
  
> Ein Zeiger auf eine durch Semikolons getrennte UNICODE-Zeichenfolge mit Parametern für die Sitzung. Excel verwendet dieses Argument nicht.
    
## <a name="return-value"></a>Rückgabewert

Eine Sitzungs-ID, die in anderen Aufrufen des Clusterconnectors verwendet werden soll, wenn die Sitzung erfolgreich erstellt wurde; andernfalls **xlHpcRetCallFailed**.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

