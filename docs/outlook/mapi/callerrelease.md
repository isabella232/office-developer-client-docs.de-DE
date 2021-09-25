---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ad1f6408b7da14027c4b84d09575d06091381371
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567844"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, die ein Tabellendatenobjekt freigeben kann, wenn eine Tabellenansicht freigegeben wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Parameter

 _ulCallerData_
  
> [in] Anruferdaten, die von mapi mit der Tabellenansicht gespeichert und an die **CALLERRELEASE-basierte** Rückruffunktion übergeben werden. Die Daten bieten Kontext zur freigegebenen Tabellenansicht. 
    
 _lpTblData_
  
> [in] Zeiger auf die [ITableData: IUnknown-Schnittstelle](itabledataiunknown.md) für das Tabellendatenobjekt, das der freigegebenen Tabellenansicht zugrunde liegt. 
    
 _lpVue_
  
> [in] Zeiger auf die [IMAPITable: IUnknown-Schnittstelle](imapitableiunknown.md) für die Tabellenansicht, die veröffentlicht wird. Dies ist eine Schnittstelle für das Tabellenobjekt, das im  _lppMAPITable-Parameter_ der [ITableData::HrGetView-Methode](itabledata-hrgetview.md) zurückgegeben wird, die das freizugebende Objekt erstellt hat. 
    
## <a name="return-value"></a>Rückgabewert

Keines 
  
## <a name="remarks"></a>HinwBemerkungeneise

Eine Clientanwendung oder ein Dienstanbieter, die ein Tabellendatenobjekt aufgefüllt hat, kann [ITableData::HrGetView](itabledata-hrgetview.md) aufrufen, um eine schreibgeschützte, sortierte Ansicht der Tabelle zu erstellen. Der Aufruf von **HrGetView** übergibt einen Zeiger an eine **CALLERRELEASE-basierte** Rückruffunktion sowie einen Kontext, der mit der Tabellenansicht gespeichert werden soll. Wenn die Referenzanzahl der Tabellenansicht auf Null zurückgibt und die Ansicht freigegeben wird, ruft die **IMAPITable-Implementierung** die Rückruffunktion auf und übergibt den Kontext im _ulCallerData-Parameter._ 
  
Eine gängige Verwendung einer **CALLERRELEASE-basierten** Rückruffunktion besteht darin, das zugrunde liegende Tabellendatenobjekt freizugeben und es während der nachfolgenden Verarbeitung nicht nachverfolgen zu müssen. 
  

