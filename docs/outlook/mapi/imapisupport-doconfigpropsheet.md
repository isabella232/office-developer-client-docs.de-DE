---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3d16b6fad12091b6e5abe3f467dff18959459fd8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596078"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Konfigurationseigenschaftenblatt an.
  
```cpp
HRESULT DoConfigPropsheet(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPSTR lpszTitle,
  LPMAPITABLE lpDisplayTable,
  LPMAPIPROP lpConfigData,
  ULONG ulTopPage
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des Eigenschaftenblatts.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpszTitle_
  
> [in] Ein Zeiger auf den Titel des Eigenschaftenblatts.
    
 _lpDisplayTable_
  
> [in] Ein Zeiger auf die Anzeigetabelle, in der die Steuerelemente beschrieben werden, die auf dem Eigenschaftenblatt angezeigt werden sollen.
    
 _lpConfigData_
  
> [in] Ein Zeiger auf die [IMAPIProp-Implementierung,](imapipropiunknown.md) die für den Zugriff auf die Konfigurationseigenschaften verwendet werden soll, die auf dem Eigenschaftenblatt angezeigt werden sollen. 
    
 _ulTopPage_
  
> [in] Ein nullbasierter Index auf der standardmäßigen oberen Seite des Eigenschaftenblatts.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Konfigurationseigenschaftenblatt wurde angezeigt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::D oConfigPropsheet-Methode** wird für alle Unterstützungsobjekte implementiert. **DoConfigPropSheet** bietet eine Standardbenutzeroberfläche zum Anzeigen der Eigenschaften von Dienstanbietern und Nachrichtendiensten. Sie sollten dieses Standarddialogfeld für alle Konfigurationseigenschaftenanzeigen verwenden, damit Benutzer von einer konsistenten Windows Schnittstelle profitieren. 
  
Dienstanbieter rufen **DoConfigPropSheet** im Rahmen der Implementierung der [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) oder über eine Schaltfläche auf, die zum Anzeigen von Details zu Eigenschaften verwendet wird. Nachrichtendienste rufen **DoConfigPropSheet** aus ihrer Nachrichtendienst-Einstiegspunktfunktion auf. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die Anzeigetabelle erstellen, auf die der  _parameter lpDisplayTable_ verweist, indem Sie die [BuildDisplayTable-Funktion](builddisplaytable.md) oder benutzerdefinierten Code aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[BuildDisplayTable](builddisplaytable.md)
  
[CreateIProp](createiprop.md)
  
[IABProvider::Logon](iabprovider-logon.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMSProvider::Logon](imsprovider-logon.md)
  
[IXPProvider::TransportLogon](ixpprovider-transportlogon.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

