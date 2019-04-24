---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Zeigt das Dialogfeld Kontoeinstellungen oder neues Konto hinzufügen an.
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322064"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Zeigt das Dialogfeld **Kontoeinstellungen** oder **Neues Konto hinzufügen** an. 
  
## <a name="quick-info"></a>QuickInfo

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a>Parameter

_hwnd_
  
> in Das Handle für das Fenster, in dem das angezeigte Dialogfeld modal ist. MöglicherWeise NULL.
    
_dwFlags_
  
> in Flags zum Ändern des Anzeigeverhaltens. 
    
   - **ACCTUI_NO_WARNING**– zeigen Sie nicht die Warnung an, dass Änderungen erst wirksam werden, wenn Outlook neu gestartet wird. Gilt nur, wenn die Anwendung in-Process mit Outlook. exe ausgeführt wird.
    
   - **ACCTUI_SHOW_DATA_TAB**– zeigt das Dialogfeld **Kontoeinstellungen** an, wobei die Registerkarte **Daten** ausgewählt ist. Gilt nur, wenn **ACCTUI_SHOW_ACCTWIZARD** nicht festgelegt ist. 
    
   - **ACCTUI_SHOW_ACCTWIZARD**– zeigt das Dialogfeld **Neues Konto hinzufügen** an. 
    
_wszTitle_
  
> in Dieser Parameter wird nicht verwendet und sollte NULL sein.
    
_cCategories_
  
> in Dieser Parameter wird nicht verwendet und muss NULL sein. 
    
_rgclsidCategories_
  
> in Dieser Parameter wird nicht verwendet und muss NULL sein.
    
_pclsidType_
  
> in Dieser Parameter wird nicht verwendet und muss NULL sein.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Anruf wurde erfolgreich ausgeführt.  <br/> |
|E_ACCT_UI_BUSY  <br/> |Das Dialogfeld konnte nicht erstellt werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Das Dialogfeld **Neues Konto hinzufügen** hat einen Fehler zurückgegeben.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |Der _cCategories_-, _RgclsidCategories_-oder _pclsidType_ -Parameter ist ungleich NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |Das Dialogfeld **Kontoeinstellungen** hat einen Fehler zurückgegeben.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die _cCategories_-, _RgclsidCategories_-und _pclsidType_ -Parameter werden zu diesem Zeitpunkt nicht verwendet und müssen NULL sein.  _wszTitle_ wird nicht verwendet und sollte auch NULL sein. 
  

