---
title: CALLERRELEASE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CALLERRELEASE
api_type:
- HeaderDef
ms.assetid: 80ba893d-3380-4db1-9175-f5b84cb57def
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9a22550e60c9de38236a9f612c7e60f50f18978f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408726"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Rückruffunktion, mit der ein Tabellendatenobjekt freigegeben werden kann, wenn eine Tabellenansicht freigegeben wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
|Definierte Funktion, die von:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Parameter

 _ulCallerData_
  
> [in] Anruferdaten, die von MAPI mit der Tabellenansicht gespeichert und an die **CALLERRELEASE-basierte** Rückruffunktion übergeben werden. Die Daten bieten Kontext zur freigegebenen Tabellenansicht. 
    
 _lpTblData_
  
> [in] Zeiger auf die [ITableData : IUnknown-Schnittstelle](itabledataiunknown.md) für das Tabellendatenobjekt, das der freigegebenen Tabellenansicht zugrunde liegt. 
    
 _lpVue_
  
> [in] Zeiger auf die [IMAPITable : IUnknown-Schnittstelle](imapitableiunknown.md) für die tabellenansicht, die freigegeben wird. Dies ist eine Schnittstelle für das Tabellenobjekt, das im  _lppMAPITable-Parameter_ der [ITableData::HrGetView-Methode](itabledata-hrgetview.md) zurückgegeben wird, die das zu veröffentlichende Objekt erstellt hat. 
    
## <a name="return-value"></a>Rückgabewert

Keine 
  
## <a name="remarks"></a>Hinweise

Eine Clientanwendung oder ein Dienstanbieter, der ein Tabellendatenobjekt aufgefüllt hat, kann [ITableData::HrGetView](itabledata-hrgetview.md) aufrufen, um eine schreibgeschützte, sortierte Ansicht der Tabelle zu erstellen. Der Aufruf von **HrGetView** übergibt einen Zeiger an eine **CALLERRELEASE-basierte** Rückruffunktion und auch einen Kontext, der mit der Tabellenansicht gespeichert werden soll. Wenn die Referenzanzahl der Tabellenansicht auf Null zurückkehrt und die Ansicht freigegeben wird, ruft die **IMAPITable-Implementierung** die Rückruffunktion auf und übergibt den Kontext im _ulCallerData-Parameter._ 
  
Eine häufige Verwendung einer **CALLERRELEASE-basierten** Rückruffunktion besteht in der Freigabe des zugrunde liegenden Tabellendatenobjekts und muss während der nachfolgenden Verarbeitung nicht nachverfolgt werden. 
  

