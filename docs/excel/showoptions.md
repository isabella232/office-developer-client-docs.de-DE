---
title: ShowOptions
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 51acac58-ec39-488f-979c-1887dc2ab94b
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5b58b71dc4f2441448eb3e0dac2c3c5763675927
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407697"
---
# <a name="showoptions"></a>ShowOptions

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Zeigt ein modales Dialogfeld zum Sammeln von Informationen vom Benutzer an. Dieser Einstiegspunkt wird aufgerufen, wenn  ein Benutzer  im Dialogfeld **Excel-Optionen** (in der Kategorie Erweitert unter dem  Abschnitt **Formeln)** neben dem Feld Clustertyp auf die Schaltfläche Optionen für den ausgewählten Clusterconnector klickt. Clusterconnectors sind für die Implementierung ihrer eigenen Dialogschnittstelle für Optionen und das Speichern der zugehörigen Daten in der Registrierung oder an anderer Stelle verantwortlich. Die Optionen sind intern für den Clusterconnector. Excel sie nicht kennen. 
  
```cpp
int ShowOptions(HWND hWndParent)
```

## <a name="parameters"></a>Parameter

_hWndParent_
  
> Ein Handle zum Excel Fenster.
    
## <a name="return-value"></a>Rückgabewert

**xlHpcRetSuccess,** wenn das Dialogfeld angezeigt wurde; **xlHpcRetCallFailed,** wenn es nicht angezeigt wurde. 
  
## <a name="remarks"></a>Hinweise

Clusterconnectors können dieses Dialogfeld verwenden, um Informationen, z. B. den zu verwendende Clusterserver, vom Benutzer zu erhalten.
  
## <a name="see-also"></a>Siehe auch

- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)

