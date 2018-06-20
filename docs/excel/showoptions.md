---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: dbf6f0f50e9f7fa988e83f3b58012e9deac13eac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790568"
---
# <a name="showoptions"></a>ShowOptions

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Zeigt ein modales Dialogfeld zum Sammeln von Informationen vom Benutzer. Dieser Einstiegspunkt wird aufgerufen, wenn ein Benutzer auf die Schaltfläche **Optionen** neben dem Feld **Clustertyp** für die ausgewählten Clusterconnector (in der Kategorie **Erweitert** im Abschnitt **Formeln** ) im Dialogfeld **Excel-Optionen** klickt. Clusterconnectoren sind verantwortlich für die Implementierung ihrer eigenen Optionen Dialogfeld-Schnittstelle und zum Speichern der verknüpften Daten in der Registrierung oder an anderer Stelle. Die Optionen sind in der Clusterconnector interne. Excel ist nicht bekannt. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Parameter

_hWndParent_
  
> Ein Handle für das Excel-Fenster.
    
## <a name="return-value"></a>R�ckgabewert

**XlHpcRetSuccess** , wenn das Dialogfeld angezeigt wurde; **XlHpcRetCallFailed** , wenn er nicht angezeigt wurde. 
  
## <a name="remarks"></a>Hinweise

In diesem Dialogfeld können clusterconnectoren zum Abrufen von Informationen, beispielsweise welche Clusterserver aus der Benutzer verwenden.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

