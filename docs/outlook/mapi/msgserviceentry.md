---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427878"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert einen Prototyp für eine Nachrichtendienst-Einstiegspunktfunktion, um die Konfiguration des Nachrichtendiensts zu unterstützen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Nachrichtendienste  <br/> |
|Definierte Funktion, die von:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT MSGSERVICEENTRY(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulContext,
  ULONG cValues,
  LPSPropValue lpProps,
  LPPROVIDERADMIN lpProviderAdmin,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>Parameter

 _hInstance_
  
> [in] Handle der Instanz des DienstanbietersDLL. Das Handle wird in der Regel zum Abrufen von Ressourcen verwendet. 
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle verfügbar** machen soll. Der Nachrichtendienst muss diese Zuordnungsmethode möglicherweise verwenden, wenn er mit bestimmten Schnittstellen wie **IStream arbeitet.** 
    
 _lpMAPISup_
  
> [in] Zeiger auf eine [IMAPISupport : IUnknown-Schnittstellenimplementierung.](imapisupportiunknown.md) 
    
 _ulUIParam_
  
> [in] Ein implementierungsspezifischer Wert, der zum Übergeben von Benutzeroberflächeninformationen an eine Funktion oder Null verwendet wird. Der  _ulUIParam-Parameter_ ist das übergeordnete Fensterhandle für das Konfigurationsdialogfeld und hat den Typ HWND (in eine ULONG_PTR). Der Wert Null gibt an, dass es kein übergeordnetes Fenster gibt. 
    
 _ulFlags_
  
> [in] Bitmaske mit Flags, die Optionen für die Diensteingabefunktion angibt. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> Die Benutzeroberfläche für die Konfiguration des Diensts sollte die aktuelle Konfiguration anzeigen, jedoch nicht zulassen, dass der Benutzer sie ändert. 
    
SERVICE_UI_ALLOWED 
  
> Ermöglicht bei Bedarf das Anzeigen eines Konfigurationsdialogfelds. Wenn das SERVICE_UI_ALLOWED festgelegt ist, sollte das Dialogfeld nur angezeigt werden, wenn das  _lpProps-Eigenschaftswertarray_ leer ist oder keine gültige Konfiguration enthält. Wenn SERVICE_UI_ALLOWED nicht festgelegt ist, wird möglicherweise weiterhin ein Dialogfeld angezeigt, wenn SERVICE_UI_ALWAYS festgelegt ist. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Fordert an, dass das Konfigurationsdialogfeld für den aktiven Anbieter über anderen Dialogfelder angezeigt wird. 
    
SERVICE_UI_ALWAYS 
  
> Der Nachrichtendienst muss ein Konfigurationsdialogfeld anzeigen. Wenn das SERVICE_UI_ALWAYS nicht festgelegt ist, wird möglicherweise weiterhin ein Konfigurationsdialogfeld angezeigt, wenn das SERVICE_UI_ALLOWED-Flag festgelegt ist und keine gültigen Konfigurationsinformationen im  _lpProps-Eigenschaftswertarray_ verfügbar sind. Entweder SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS müssen so festgelegt sein, dass eine Benutzeroberfläche angezeigt werden kann. 
    
 _ulContext_
  
> [in] Der Konfigurationsvorgang, den MAPI derzeit ausführen. Der  _ulContext-Parameter_ enthält einen der folgenden Werte: 
    
MSG_SERVICE_CONFIGURE 
  
> Änderungen an der Konfiguration des Diensts sollten im Profil vorgenommen werden. Wenn das SERVICE_UI_ALWAYS festgelegt ist, sollte der Dienst sein Konfigurationsdialogfeld anzeigen. Das Dialogfeld sollte auch angezeigt werden, wenn das SERVICE_UI_ALLOWED festgelegt ist und der  _lpProps-Parameter_ leer ist oder keine gültigen Konfigurationsdaten enthält. Wenn  _lpProps_ gültige Daten enthält, sollte kein Dialogfeld angezeigt werden, und der Dienst sollte diese Daten für die Konfigurationsänderung verwenden. 
    
MSG_SERVICE_CREATE 
  
> Der Dienst wird einem Profil hinzugefügt. Wenn das SERVICE_UI_ALWAYS oder SERVICE_UI_ALLOWED festgelegt ist, sollte der Dienst sein Konfigurationsdialogfeld anzeigen. Wenn keines der Kennzeichen festgelegt ist, sollte der Dienst fehlschlagen. 
    
MSG_SERVICE_DELETE 
  
> Der Dienst wird aus einem Profil entfernt. Nachdem dieses Ereignis empfangen wurde, sollte der Dienst S_OK.
    
MSG_SERVICE_INSTALL 
  
> Der Dienst wurde auf der Arbeitsstation des Benutzers über ein Netzwerk, eine Diskette oder ein anderes externes Medium installiert. Nach dem Empfang dieses Ereignisses gibt der Dienst in der Regel S_OK. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Fordert an, dass der Dienst eine zusätzliche Instanz eines Anbieters erstellt. Wenn der Dienst diesen Vorgang unterstützt, sollte [er IProviderAdmin::CreateProvider aufrufen.](iprovideradmin-createprovider.md) Wenn der Dienst diesen Vorgang nicht unterstützt, kann er MAPI_E_NO_SUPPORT. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Fordert an, dass der Dienst eine Anbieterinstanz löscht. Wenn der Dienst diesen Vorgang unterstützt, sollte er [IProviderAdmin::D eleteProvider aufrufen.](iprovideradmin-deleteprovider.md) Wenn der Dienst diesen Vorgang nicht unterstützt, kann er MAPI_E_NO_SUPPORT.
    
MSG_SERVICE_UNINSTALL 
  
> Der Dienst wird entfernt. Nach dem Empfang dieses Ereignisses kann der Dienst alle Bereinigungsaufgaben ausführen, die vor dem Ende des Diensts ausgeführt werden sollten, und dann mit einem Erfolgswert zurückgeben. Wenn der Benutzer die Entfernung abbricht, sollte der Dienst MAPI_E_USER_CANCEL. 
    
 _cValues_
  
> [in] Anzahl der Eigenschaftswerte im Array, auf die der  _lpProps-Parameter_ verweist. Der Wert des  _cValues-Parameters_ ist null, wenn MAPI keine Eigenschaftswerte übergeben. 
    
 _lpProps_
  
> [in] Zeiger auf ein optionales Array von [SPropValue-Strukturen,](spropvalue.md) das Werte für vom Anbieter unterstützte Eigenschaften angibt, die die Funktion beim Konfigurieren des Nachrichtendiensts verwendet. Die Funktion verwendet diesen Parameter nur, wenn  _der ulContext-Parameter_ auf MSG_SERVICE_CONFIGURE. Dieser Parameter wird häufig verwendet, um den Pfad zu einer Datei für einen dateibasierten Dienst, z. B. einen persönlichen Adressbuchdienst, zu übergeben. Wenn das MSG_SERVICE_CONFIGURE im  _ulFlags-Parameter_ nicht übergeben wird, muss  _der lpProps-Parameter_ null sein. 
    
 _lpProviderAdmin_
  
> [in] Zeiger auf eine [IProviderAdmin:IUnknown-Schnittstelle,](iprovideradminiunknown.md) die die Funktion zum Suchen von Profilabschnitten für einen bestimmten Anbieter im aktuellen Nachrichtendienst verwenden kann. 
    
 _lppMapiError_
  
> [out] Zeiger auf eine [MAPIERROR-Struktur.](mapierror.md) Die Struktur wird mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) zugewiesen. Alle Member sind optional, obwohl die meisten Strukturen eine gültige Fehlermeldungszeichenfolge im  _lpszError-Element_ enthalten. Wenn  _die lpszComponent-_ oder  _lpszError-Elemente_ der Struktur vorhanden sind, muss ihr Arbeitsspeicher schließlich durch einen einzelnen Aufruf von [MAPIFreeBuffer](mapifreebuffer.md) in der Basisstruktur frei werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_UNCONFIGURED 
  
> Der Dienstanbieter wurde nicht konfiguriert. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
MAPI_E_NO_SUPPORT 
  
> Der Anbieter unterstützt entweder keine Änderungen an seinen Objekten oder keine Benachrichtigung über Änderungen. 
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Hinweise

Eine funktion, die mithilfe des **MSGSERVICEENTRY-Funktionsprototyps** definiert wurde, ermöglicht Nachrichtendiensten, sich selbst zu konfigurieren oder andere dienstspezifische Aktionen durchzuführen. Die Funktion bietet in erster Linie ein Dialogfeld, in dem der Benutzer einstellungen speziell für den Nachrichtendienst ändern kann. Sie kann auch die programmgesteuerte Konfiguration mithilfe des Eigenschaftswertarrays unterstützen, das im  _lpProps-Parameter übergeben_ wird. Die programmgesteuerte Konfiguration ist optional, es sei denn, der Dienst unterstützt den Profil-Assistenten, für den er erforderlich ist. 
  
MAPI ruft diesen Einstiegspunkt aus der Systemsteuerungsanwendung oder als Reaktion auf eine Clientanwendung auf, die [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) oder [IMsgServiceAdmin::ConfigureMsgService aufruft.](imsgserviceadmin-configuremsgservice.md) 
  
MAPI legt keine Einschränkung auf den Funktionsnamen fest, den ein Nachrichtendienst für den **MSGSERVICEENTRY-Prototyp** verwendet, bevorzugt jedoch den Namen **ServiceEntry**. Es gibt keine Einschränkung für die Ordnungszahl für die Funktion, und eine einzelne Anbieter-DLL kann mehrere Funktionen enthalten. Allerdings kann nur eine der Funktionen den Namen **ServiceEntry haben.** 
  
Ein Nachrichtendienst kann die [BuildDisplayTable-Funktion](builddisplaytable.md) und die [IMAPISupport::D oConfigPropsheet-Methode](imapisupport-doconfigpropsheet.md) verwenden, um die Implementierung des Konfigurationsdialogfelds zu vereinfachen. 
  
Ein Benutzer kann einen Vorgang MSG_SERVICE_UNINSTALL abbrechen. In diesem Fall sollte die **ServiceEntry-Funktion** mit dem Benutzer überprüfen, ob der Dienst nicht entfernt werden soll, und MAPI_E_USER_CANCEL, wenn der Dienst installiert bleibt. 
  
Eine Funktion, die auf dem **MSGSERVICEENTRY-Prototyp** basiert, gibt einen der aufgeführten HRESULT-Werte zurück. MAPI gibt diesen Wert weiter, wenn er auf den Aufruf eines Clients an [IMsgServiceAdmin::ConfigureMsgService reagiert.](imsgserviceadmin-configuremsgservice.md) 
  
Nachrichtendienste, die eine Diensteintragsfunktion exportieren, müssen die **Eigenschaften PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) und **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) im Nachrichtendienstabschnitt von MAPISVC.INF enthalten. 
  

