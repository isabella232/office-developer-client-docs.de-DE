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
  
Definiert eine Rückruffunktion, die ein Tabellendaten Objekt freigeben kann, wenn eine Tabellenansicht veröffentlicht wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Parameter

 _ulCallerData_
  
> in Von MAPI gespeicherte Anrufer-Daten in der Tabellenansicht und an die **CALLERRELEASE** -basierte Rückruffunktion übergeben. Die Daten liefern Kontext über die Tabellenansicht, die freigegeben wird. 
    
 _lpTblData_
  
> in Zeiger auf die [ITableData: IUnknown](itabledataiunknown.md) -Schnittstelle für das Tabellendaten Objekt, das der Tabellenansicht zugrunde liegt, die freigegeben wird. 
    
 _lpVue_
  
> in Zeiger auf die [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle für die Tabellenansicht, die freigegeben wird. Hierbei handelt es sich um eine Schnittstelle für das Table-Objekt, das im _lppMAPITable_ -Parameter der [ITableData:: HrGetView](itabledata-hrgetview.md) -Methode zurückgegeben wird, die das Release-Objekt erstellt hat. 
    
## <a name="return-value"></a>Rückgabewert

Keine 
  
## <a name="remarks"></a>Bemerkungen

Eine Clientanwendung oder ein Dienstanbieter, der ein Tabellendaten Objekt aufgefüllt hat, kann [ITableData:: HrGetView](itabledata-hrgetview.md) aufrufen, um eine schreibgeschützte, sortierte Ansicht der Tabelle zu erstellen. Der Aufruf von **HrGetView** übergibt einen Zeiger auf eine **CALLERRELEASE** -basierte Rückruffunktion und auch einen Kontext, der mit der Tabellenansicht gespeichert werden soll. Wenn der Verweiszähler der Tabellenansicht auf Null zurückgesetzt wird und die Ansicht veröffentlicht wird, ruft die **IMAPITable** -Implementierung die Rückruffunktion auf und übergibt den Kontext im _ulCallerData_ -Parameter. 
  
Eine häufige Verwendung einer **CALLERRELEASE** -basierten Rückruffunktion besteht darin, das zugrunde liegende Tabellendaten Objekt freizusetzen und es während der nachfolgenden Verarbeitung nicht nachzuverfolgen. 
  

