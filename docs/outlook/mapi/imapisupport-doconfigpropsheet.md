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
ms.openlocfilehash: 3b3499de9446c83cfc3b97b4d6b02e7c430b65f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586396"
---
# <a name="imapisupportdoconfigpropsheet"></a>IMAPISupport::DoConfigPropsheet

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zeigt eine Konfiguration Eigenschaftenblatt.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster im Eigenschaftsfenster.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpszTitle_
  
> [in] Ein Zeiger auf den Titel des Eigenschaftenblatts.
    
 _lpDisplayTable_
  
> [in] Ein Zeiger auf den zeigt die Tabelle, die angezeigt werden, um die Steuerelemente auf der Eigenschaftenseite beschreibt.
    
 _lpConfigData_
  
> [in] Ein Zeiger auf die Implementierung [IMAPIProp](imapipropiunknown.md) , für den Zugriff auf die Konfigurationseigenschaften verwendet werden, auf der Eigenschaftenseite angezeigt werden. 
    
 _ulTopPage_
  
> [in] Ein nullbasierter Index der oberen Standardseite des Eigenschaftenblatts.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Eigenschaftenblatt Konfiguration wurde angezeigt.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPISupport::DoConfigPropsheet** -Methode wird für alle Unterstützungsobjekte implementiert. **DoConfigPropSheet** stellt eine Standardbenutzeroberfläche zum Anzeigen der Eigenschaften der Dienstanbieter und Message-Dienste. Sie sollten dieses Dialogfeld standard für alle Konfiguration-Eigenschaft zeigt verwenden, damit Benutzer eine konsistente Schnittstelle Windows nutzen. 
  
Dienstanbieter anrufen **DoConfigPropSheet** als Teil ihrer Implementierung [der SettingsDialog](imapistatus-settingsdialog.md) oder eine Schaltfläche zum Anzeigen von Details auf Eigenschaften. Nachricht Services Aufrufen **DoConfigPropSheet** aus ihrer Nachricht Service Entry Point-Funktion. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die Anzeige-Tabelle der _LpDisplayTable_ -Parameter auf das durch Aufrufen der [BuildDisplayTable](builddisplaytable.md) -Funktion oder mit benutzerdefiniertem Code erstellen. 
  
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

