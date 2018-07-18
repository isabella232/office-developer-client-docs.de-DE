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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 69ee06ef8c8f5499dec41232d3dc7b374b15a744
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791370"
---
# <a name="callerrelease"></a>CALLERRELEASE

  
  
**Betrifft**: Outlook 
  
Definiert eine Rückruffunktion, die ein Table-Datenobjekt freigeben kann, wenn eine Tabellenansicht freigegeben wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
|Definierte Funktion aufgerufen:  <br/> |MAPI  <br/> |
   
```cpp
void CALLERRELEASE(
  ULONG_PTR ulCallerData,
  LPTABLEDATA lpTblData,
  LPMAPITABLE lpVue
);
```

## <a name="parameters"></a>Parameter

 _ulCallerData_
  
> [in] Anrufer-Daten mit der Tabellenansicht MAPI gespeichert und an die **CALLERRELEASE** übergebenen basieren Callback-Funktion. Die Daten enthält Kontext über die Tabellenansicht freigegeben wird. 
    
 _lpTblData_
  
> [in] Zeiger auf die [ITableData: IUnknown](itabledataiunknown.md) Schnittstelle für die Tabelle Datenobjekt zugrunde liegenden der Tabellenansicht freigegeben wird. 
    
 _lpVue_
  
> [in] Zeiger auf die [IMAPITable: IUnknown](imapitableiunknown.md) -Schnittstelle für die Tabellenansicht freigegeben wird. Dies ist eine Schnittstelle für das Table-Objekt zurückgegeben, die im Parameter _LppMAPITable_ der [ITableData::HrGetView](itabledata-hrgetview.md) -Methode, die das freizugebende-Objekt erstellt. 
    
## <a name="return-value"></a>R�ckgabewert

Keine 
  
## <a name="remarks"></a>Bemerkungen

Eine Clientanwendung oder Dienstanbieter, die ein Table-Datenobjekt gefüllt wurde kann [ITableData::HrGetView](itabledata-hrgetview.md) zum Erstellen einer Ansicht, sortierten der Tabelle aufrufen. Der Anruf an **HrGetView** übergibt einen Zeiger auf eine Rückruffunktion **CALLERRELEASE** basiert und auch einen Kontext mit der Tabellenansicht gespeichert werden soll. Wenn der Tabellenansicht der Referenzzähler gibt 0 (null) zurück, und die Ansicht wird veröffentlicht, ruft die **IMAPITable** -Implementierung die Callback-Funktion, die im Kontext der _UlCallerData_ -Parameter übergeben. 
  
Eine häufige Verwendung von einer Rückruffunktion **CALLERRELEASE** basierend ist zum Freigeben des zugrunde liegenden Daten Tabellenobjekts und keinen verfolgen sie bei der nachfolgenden Verarbeitung an. 
  

