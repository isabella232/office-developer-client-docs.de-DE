---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Zeigt das Dialogfeld Konto Einstellungen oder Neues Konto hinzufügen an.
ms.openlocfilehash: 22a9165fa5cd29e0f9da9de64c243806e6fb1712
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561922"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a>IOlkAccountManager::DisplayAccountList

Zeigt das Dialogfeld **Konto Einstellungen** oder **Neues Konto hinzufügen** an. 
  
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
  
> [in] Das Handle für das Fenster, an das das angezeigte Dialogfeld gebunden ist. Kann Null sein.
    
_Dwflags_
  
> [in] Kennzeichen zum Ändern des Verhaltens der Anzeige. 
    
   - **ACCTUI_NO_WARNING**: Zeigen Sie nicht die Warnung an, dass Änderungen erst wirksam werden, wenn Outlook neu gestartet wird. Gilt nur, wenn die Anwendung innerhalb des Prozesses mit Outlook.exe ausgeführt wird.
    
   - **ACCTUI_SHOW_DATA_TAB**- Zeigt das Dialogfeld **"Konto Einstellungen"** an, in dem die Registerkarte **"Daten"** ausgewählt ist. Nur gültig, wenn **ACCTUI_SHOW_ACCTWIZARD** nicht festgelegt ist. 
    
   - **ACCTUI_SHOW_ACCTWIZARD**: Zeigt das Dialogfeld **"Neues Konto hinzufügen"** an. 
    
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
|S_OK  <br/> |Der Anruf war erfolgreich.  <br/> |
|E_ACCT_UI_BUSY  <br/> |Das Dialogfeld konnte nicht erstellt werden.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |Konto-Manager wurde nicht für die Verwendung initialisiert.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Im Dialogfeld **"Neues Konto hinzufügen" wurde** ein Fehler zurückgegeben.  <br/> |
|MAPI_E_INVALID_PARAMETER  <br/> |Der  _Parameter "cCategories",_  _"rgclsidCategories"_ oder  _"pclsidType"_ ist ungleich NULL.  <br/> |
|MAPI_E_USER_CANCEL  <br/> |Im Dialogfeld **Konto Einstellungen** wurde ein Fehler zurückgegeben.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Parameter  _"cCategories",_  _"rgclsidCategories"_ und  _"pclsidType"_ werden derzeit nicht verwendet und müssen NULL sein.  _wszTitle_ wird nicht verwendet und sollte auch NULL sein. 
  

