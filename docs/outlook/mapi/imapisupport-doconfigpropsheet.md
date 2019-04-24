---
title: IMAPISupportDoConfigPropsheet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoConfigPropsheet
api_type:
- COM
ms.assetid: 3899c49c-a0ec-4dca-92e8-e801cd4908cf
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cd8727104af694d456074614b5ea7c222c9b91b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322372"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Konfigurationseigenschaften Fenster an.
  
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
  
> in Ein Handle für das übergeordnete Fenster des Eigenschaftenblatts.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpszTitle_
  
> in Ein Zeiger auf den Titel des Eigenschaftenblatts.
    
 _lpDisplayTable_
  
> in Ein Zeiger auf die Anzeigetabelle, in der die Steuerelemente beschrieben werden, die im Eigenschaftenfenster angezeigt werden sollen.
    
 _lpConfigData_
  
> in Ein Zeiger auf die [IMAPIProp](imapipropiunknown.md) -Implementierung, die für den Zugriff auf die Konfigurationseigenschaften verwendet werden soll, die im Eigenschaftenfenster angezeigt werden sollen. 
    
 _ulTopPage_
  
> in Ein nullbasierter Index auf der oberen Standardseite des Eigenschaftenblatts.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Konfigurationseigenschaften Blatt wurde angezeigt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPISupport::D oconfigpropsheet** -Methode wird für alle Support-Objekte implementiert. **DoConfigPropSheet** bietet eine Standardbenutzeroberfläche zum Anzeigen der Eigenschaften von Dienstanbietern und Nachrichtendiensten. Sie sollten dieses Standarddialogfeld für alle Konfigurationseigenschaften anzeigen verwenden, damit die Benutzer von einer konsistenten Windows-Oberfläche profitieren. 
  
Dienstanbieter rufen **DoConfigPropSheet** als Teil ihrer Implementierung der [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) -Methode oder einer Schaltfläche auf, die zum Anzeigen von Details zu Eigenschaften verwendet wird. Nachrichtendienste rufen **DoConfigPropSheet** über die Einstiegspunktfunktion des Nachrichtendiensts auf. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die Anzeigetabelle, auf die durch den _lpDisplayTable_ -Parameter verwiesen wird, durch Aufrufen der [BuildDisplayTable](builddisplaytable.md) -Funktion oder mit benutzerdefiniertem Code erstellen. 
  
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

