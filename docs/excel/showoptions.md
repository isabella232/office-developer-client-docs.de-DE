---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2fb8616fafd778a6dbd8bf990b2e7b13ffcc7175
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572375"
---
# <a name="showoptions"></a>ShowOptions

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Zeigt ein modales Dialogfeld zum Sammeln von Informationen vom Benutzer an. Dieser Einstiegspunkt wird aufgerufen, wenn ein Benutzer im Dialogfeld **Excel Optionen** (in der Kategorie **"Erweitert"** im Abschnitt "Formeln") auf die Schaltfläche **"Optionen"** neben dem **Feld "Clustertyp"** für den ausgewählten Clusterkonnektor **klickt.** Clusterconnectors sind für die Implementierung ihrer eigenen Optionsdialogschnittstelle und das Speichern der zugehörigen Daten in der Registrierung oder an anderer Stelle verantwortlich. Die Optionen sind für den Clusterconnector intern. Excel diese nicht kennen. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Parameter

_hWndParent_
  
> Ein Handle für das Excel Fenster.
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess,** wenn das Dialogfeld angezeigt wurde; **xlHpcRetCallFailed,** wenn es nicht angezeigt wurde. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Clusterconnectors können dieses Dialogfeld verwenden, um Informationen vom Benutzer abzurufen, z. B. welchen Clusterserver er verwenden soll.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

