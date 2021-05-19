---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Zeigt entweder das Dialogfeld Konto Einstellungen oder Das Dialogfeld Neues Konto hinzufügen an.
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415033"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Zeigt entweder **das** Einstellungen **oder das Dialogfeld Neues Konto** hinzufügen an. 
  
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
  
> [in] Das Handle zu dem Fenster, zu dem das angezeigte Dialogfeld modal ist. Kann null sein.
    
_dwFlags_
  
> [in] Flags zum Ändern des Anzeigeverhaltens. 
    
   - **ACCTUI_NO_WARNING**– Zeigen Sie die Warnung nicht an, dass Änderungen erst wirksam werden, wenn Outlook neu gestartet wird. Gilt nur, wenn die Anwendung mit einem Outlook.exe.
    
   - **ACCTUI_SHOW_DATA_TAB**– Zeigt das Dialogfeld **Konto Einstellungen,** wenn die Registerkarte **Daten** ausgewählt ist. Nur gültig, **ACCTUI_SHOW_ACCTWIZARD** nicht festgelegt ist. 
    
   - **ACCTUI_SHOW_ACCTWIZARD**– Zeigt das **Dialogfeld Neues Konto** hinzufügen an. 
    
_wszTitle_
  
> [in] Dieser Parameter wird nicht verwendet und sollte NULL sein.
    
_cCategories_
  
> [in] Dieser Parameter wird nicht verwendet und muss NULL sein. 
    
_rgclsidCategories_
  
> [in] Dieser Parameter wird nicht verwendet und muss NULL sein.
    
_pclsidType_
  
> [in] Dieser Parameter wird nicht verwendet und muss NULL sein.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_UI_BUSY  <br/> |Das Dialogfeld konnte nicht erstellt werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Im **Dialogfeld Neues Konto** hinzufügen wurde ein Fehler zurückgegeben.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |Der  _Parameter cCategories_,  _rgclsidCategories_ oder  _pclsidType_ ist nicht NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |Im **Einstellungen** Dialogfeld Konto wurde ein Fehler zurückgegeben.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die  _Parameter cCategories,_  _rgclsidCategories_ und  _pclsidType_ werden derzeit nicht verwendet und müssen NULL sein.  _wszTitle_ wird nicht verwendet und sollte auch NULL sein. 
  

