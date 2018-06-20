---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Dialogfeld Kontoeinstellungen oder neues Konto hinzufügen angezeigt.
ms.openlocfilehash: 3c7c433eb4d8f316d32b6cd12bbbbb0e1a1cee43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791098"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Dialogfeld für die **Kontoeinstellungen** oder **Hinzufügen eines neuen Kontos** angezeigt. 
  
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
  
> [in] Das Handle für das Fenster, das angezeigte Dialogfeld gebunden werden. Möglicherweise 0 (null).
    
_dwFlags_
  
> [in] Kennzeichen, die um das Verhalten der Anzeige zu ändern. 
    
   - **ACCTUI_NO_WARNING**– die Warnung, dass die Änderungen erst in Kraft, werden Outlook gestartet wird nicht angezeigt. Gilt nur, wenn die Anwendung ausgeführt wird in-Process mit Outlook.exe befindet.
    
   - **ACCTUI_SHOW_DATA_TAB**– zeigt das Dialogfeld **Kontoeinstellungen** mit der Registerkarte **Daten** ausgewählt. Nur gültig, wenn **ACCTUI_SHOW_ACCTWIZARD** nicht festgelegt ist. 
    
   - **ACCTUI_SHOW_ACCTWIZARD**– zeigt das Dialogfeld **Neues Konto hinzufügen** . 
    
_wszTitle_
  
> [in] Dieser Parameter wird nicht verwendet und sollte NULL sein.
    
_cCategories_
  
> [in] Dieser Parameter wird nicht verwendet und muss NULL sein. 
    
_rgclsidCategories_
  
> [in] Dieser Parameter wird nicht verwendet und muss NULL sein.
    
_pclsidType_
  
> [in] Dieser Parameter wird nicht verwendet und muss NULL sein.
    
## <a name="return-values"></a>Rückgabewerte

|**[HRESULT]**|**Beschreibung**|
|:-----|:-----|
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
|E_ACCT_UI_BUSY  <br/> |Das Dialogfeld konnte nicht erstellt werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Das Dialogfeld **Neues Konto hinzufügen** zurückgegeben einen Fehler.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |Der Parameter _cCategories_, _RgclsidCategories_oder _PclsidType_ ist ungleich NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |Das Dialogfeld **Kontoeinstellungen** hat einen Fehler zurückgegeben.  <br/> |
   
## <a name="remarks"></a>Hinweise

Der Parameter _cCategories_, _RgclsidCategories_und _PclsidType_ zu diesem Zeitpunkt nicht verwendet werden und müssen NULL sein.  _WszTitle_ wird nicht verwendet und sollte auch NULL sein. 
  

