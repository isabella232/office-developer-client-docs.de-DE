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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429015"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zeigt ein Konfigurationseigenschaftsblatt an.
  
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
  
> [in] Ein Handle zum übergeordneten Fenster des Eigenschaftenblatts.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpszTitle_
  
> [in] Ein Zeiger auf den Titel des Eigenschaftenblatts.
    
 _lpDisplayTable_
  
> [in] Ein Zeiger auf die Anzeigetabelle, in der die Steuerelemente beschrieben werden, die auf dem Eigenschaftenblatt angezeigt werden sollen.
    
 _lpConfigData_
  
> [in] Ein Zeiger auf die [IMAPIProp-Implementierung,](imapipropiunknown.md) die für den Zugriff auf die Konfigurationseigenschaften verwendet werden soll, die auf dem Eigenschaftenblatt angezeigt werden sollen. 
    
 _ulTopPage_
  
> [in] Ein nullbasierter Index zur Standardmäßigen oberen Seite des Eigenschaftenblatts.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Konfigurationseigenschaftsblatt wurde angezeigt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPISupport::D oConfigPropsheet-Methode** wird für alle Supportobjekte implementiert. **DoConfigPropSheet** bietet eine Standardbenutzerschnittstelle zum Anzeigen der Eigenschaften von Dienstanbietern und Nachrichtendiensten. Verwenden Sie dieses Standarddialogfeld für alle Konfigurationseigenschaftsanzeigen, damit Benutzer von einer konsistenten Windows profitieren. 
  
Dienstanbieter rufen **DoConfigPropSheet** im Rahmen der Implementierung der [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) oder über eine Schaltfläche auf, die zum Anzeigen von Details zu Eigenschaften verwendet wird. Nachrichtendienste rufen **DoConfigPropSheet über** die Einstiegspunktfunktion des Nachrichtendiensts auf. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die Anzeigetabelle erstellen, auf die der  _lpDisplayTable-Parameter_ verweist, indem Sie die [BuildDisplayTable-Funktion](builddisplaytable.md) oder benutzerdefinierten Code aufrufen. 
  
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

