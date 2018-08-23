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
ms.openlocfilehash: 954609cbc62039c0d60874bde83fde50d1d11c30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591667"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Definiert einen Prototyp für eine Nachricht Service-Einstiegspunkt zu Nachricht Dienstkonfiguration zu unterstützen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |Message-Dienste  <br/> |
|Definierte Funktion aufgerufen:  <br/> |MAPI  <br/> |
   
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
  
> [in] Handle der Instanz von dem Dienst ProviderDLL. Das Handle ist in der Regel verwendet, um Ressourcen abzurufen. 
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE **IMalloc** -Schnittstelle verfügbar macht. Message-Dienst müssen möglicherweise beim Arbeiten mit bestimmte Schnittstellen wie **IStream**diese Zuordnungsmethode verwenden. 
    
 _lpMAPISup_
  
> [in] Zeiger auf eine [IMAPISupport: IUnknown](imapisupportiunknown.md) Schnittstelle Implementierung. 
    
 _ulUIParam_
  
> [in] Einen implementierungsspezifischen Wert für die Übergabe von Informationen zur Benutzeroberfläche für eine Funktion oder 0 (null) verwendet. Der Parameter _UlUIParam_ ist das übergeordnete Fensterhandle für das Dialogfeld Konfiguration und vom Typ HWND (Umwandlung in ein ULONG_PTR). Der Wert 0 gibt an, dass kein übergeordnetes Fenster vorhanden ist. 
    
 _ulFlags_
  
> [in] Bitmaske aus Flags, die Optionen für die Funktion Eintrag angibt. Die folgenden Kennzeichen können festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> Der Dienst Konfigurationsbenutzeroberfläche sollte zeigen Sie die aktuelle Konfiguration jedoch nicht durch den Benutzer zu ändern. 
    
SERVICE_UI_ALLOWED 
  
> Ermöglicht eine Konfigurationsdialogfeld, bei Bedarf angezeigt werden soll. Wenn das Flag SERVICE_UI_ALLOWED festgelegt ist, sollte das Dialogfeld werden nur angezeigt, wenn Wertearray der _LpProps_ -Eigenschaft leer ist oder enthält keine gültige Konfiguration. Wenn SERVICE_UI_ALLOWED nicht festgelegt ist, kann ein Dialogfeld weiterhin angezeigt werden, wenn das Flag SERVICE_UI_ALWAYS festgelegt ist. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Fordert an, dass das Dialogfeld Konfiguration für den aktiven Anbieter über andere Dialogfelder angezeigt werden. 
    
SERVICE_UI_ALWAYS 
  
> Erfordert den Dienst ein Konfigurationsdialogfeld angezeigt. Wenn das Flag SERVICE_UI_ALWAYS nicht festgelegt ist, kann ein Konfigurationsdialogfeld weiterhin angezeigt werden, wenn das Flag SERVICE_UI_ALLOWED festgelegt ist und gültige Konfigurationsinformationen nicht verfügbar aus Wertearray _LpProps_ -Eigenschaft ist. SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS muss festgelegt werden, um eine Benutzeroberfläche anzuzeigende zu ermöglichen. 
    
 _ulContext_
  
> [in] Der Vorgang zur Konfiguration, mit dem MAPI derzeit ausgeführt wird. Der Parameter _UlContext_ wird einer der folgenden Werte enthalten: 
    
MSG_SERVICE_CONFIGURE 
  
> Konfiguration des Dienstes sollte im Profil geändert werden. Wenn das Flag SERVICE_UI_ALWAYS festgelegt ist, sollte der Dienst seine Konfigurationsdialogfeld angezeigt werden. Das Dialogfeld sollte auch angezeigt werden, wenn das Flag SERVICE_UI_ALLOWED festgelegt ist und der Parameter _LpProps_ ist leer oder enthält keine gültigen Konfigurationsdaten. Wenn _LpProps_ gültige Daten enthält, kein Dialogfeld angezeigt werden soll, und der Dienst sollte diese Daten zur Erhebung von der Änderung der Konfiguration verwenden. 
    
MSG_SERVICE_CREATE 
  
> Der Dienst wird zu einem Profil hinzugefügt. Wenn die SERVICE_UI_ALWAYS oder SERVICE_UI_ALLOWED-Flag festgelegt ist, sollte der Dienst seine Konfigurationsdialogfeld angezeigt werden. Wenn weder Flag festgelegt ist, sollte der Dienst fehlschlagen. 
    
MSG_SERVICE_DELETE 
  
> Der Dienst wird aus einem Profil entfernt. Nach dem dieses Ereignis empfangen, sollte der Dienst S_OK zurückgegeben.
    
MSG_SERVICE_INSTALL 
  
> Der Dienst wurde von einem Netzwerk, Diskette oder anderen externen Datenträger auf dem Computer des Benutzers installiert. Wenn dieses Ereignis empfangen haben, gibt der Dienst in der Regel S_OK zurück. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Fordert, dass der Dienst eine zusätzliche Instanz eines Anbieters erstellen. Wenn der Dienst diesen Vorgang unterstützt, sollten sie [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md)aufrufen. Wenn der Dienst diesen Vorgang nicht unterstützt, kann MAPI_E_NO_SUPPORT zurückgegeben werden. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Fordert, dass der Dienst eine Anbieterinstanz löschen. Wenn der Dienst diesen Vorgang unterstützt, sollten sie [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md)aufrufen. Wenn der Dienst diesen Vorgang nicht unterstützt, kann MAPI_E_NO_SUPPORT zurückgegeben werden.
    
MSG_SERVICE_UNINSTALL 
  
> Der Dienst wurde entfernt. Nach dem dieses Ereignis empfangen, kann der Dienst alle Cleanup Aufgaben, bei denen erfolgen soll, bevor der Dienst beendet, und klicken Sie dann mit einem Erfolgswert zurück. Wenn der Benutzer die Entfernung abbricht, sollte der Dienst MAPI_E_USER_CANCEL zurückgegeben. 
    
 _cValues_
  
> [in] Anzahl der Eigenschaftswerte im Array auf den durch den Parameter _LpProps_ verwiesen. Der Wert des Parameters _cValues_ ist 0 (null), wenn MAPI keine Eigenschaftswerte übergeben wird. 
    
 _lpProps_
  
> [in] Zeiger auf ein optionales Array von [SPropValue](spropvalue.md) Strukturen, der Werte für Anbieter unterstützten Eigenschaften, die die Funktion verwendet wird, konfigurieren Sie den Dienst. Die Funktion verwendet diesen Parameter nur, wenn der Parameter _UlContext_ auf MSG_SERVICE_CONFIGURE festgelegt ist. Dieser Parameter wird häufig zum übergeben Sie des Pfads für eine Datei-basierten Dienst, beispielsweise eine persönliche Adressbuchdienst in einer Datei verwendet. Wenn das Flag MSG_SERVICE_CONFIGURE nicht in der _UlFlags_ -Parameter übergeben wird, muss der Parameter _LpProps_ 0 (null) sein. 
    
 _lpProviderAdmin_
  
> [in] Zeiger auf eine [IProviderAdmin:IUnknown](iprovideradminiunknown.md) -Schnittstelle, die die Funktion zum Ermitteln von Abschnitten Profil für einen bestimmten Anbieter in der aktuellen Nachrichtendienst verwenden kann. 
    
 _lppMapiError_
  
> [out] Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur. Die Struktur wird mit der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) zugeordnet. Alle Mitglieder sind optional, obwohl die meisten Strukturen auf eine Meldungszeichenfolge gültige Fehler im _LpszError_ -Member enthalten soll. Wenn die _LpszComponent_ oder _LpszError_ Member der Struktur vorhanden sind, muss ihre Speicher schließlich durch einen einzigen Aufruf von [MAPIFreeBuffer](mapifreebuffer.md) auf der Basis Struktur freigegeben werden. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_UNCONFIGURED 
  
> Der Dienstanbieter wurde nicht konfiguriert. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. 
    
MAPI_E_NO_SUPPORT 
  
> Der Anbieter unterstützt keine Änderungen auf Objekte, oder Benachrichtigung über Änderungen wird nicht unterstützt. 
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder die Option MAPI_UNICODE festgelegt wurde und die Implementierung unterstützt keine Unicode oder Parameter MAPI_UNICODE nicht festgelegt wurde und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Funktion, mit dem **MSGSERVICEENTRY** Funktionsprototyp definiert ermöglicht Message Dienste so konfigurieren Sie selbst oder andere dienstspezifische Aktionen auszuführen. Die Funktion stellt bereit in erster Linie ein Dialogfeld, in dem der Benutzer den Dienst spezifischen Einstellungen ändern kann. Sie können auch programmgesteuerte Konfiguration unterstützt werden mithilfe des im _LpProps_ -Parameter übergebenen Wertearrays-Eigenschaft. Programmgesteuerte Konfiguration ist optional, es sei denn, der Dienst der Profil-Assistent unterstützt, ist es erforderlich. 
  
MAPI-Aufrufen dieser Einstiegspunkt in der Systemsteuerung auf oder als Antwort auf eine Clientanwendung [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) oder [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)aufrufen. 
  
MAPI platziert keine Einschränkung auf den Funktionsnamen, dass eine Message Service für den **MSGSERVICEENTRY** Prototyp verwendet aber den Namen **ServiceEntry**bevorzugt. Es gibt keine Beschränkung für die Ordinal-Eigenschaft für die Funktion, und ein einzigen Anbieter DLL kann mehr als eine Funktion enthalten. Allerdings kann nur eine der Funktionen **ServiceEntry**heißen. 
  
Eine Message Service können die [BuildDisplayTable](builddisplaytable.md) -Funktion und die [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) -Methode Sie um Konfiguration Dialogfeld Feld Implementierung zu vereinfachen. 
  
Es ist möglich, dass ein Benutzer einen MSG_SERVICE_UNINSTALL-Vorgang abbrechen. In diesem Fall sollten die **ServiceEntry** -Funktion überprüfen, mit dem Benutzer, um sicherzustellen, dass der Dienst sollte nicht entfernt werden und MAPI_E_USER_CANCEL zurückgeben, wenn der Dienst nicht deinstalliert wird. 
  
Eine Funktion, die basierend auf den **MSGSERVICEENTRY** Prototyp gibt eine der aufgeführten HRESULT-Werte. MAPI weiterleitet diesen Wert, wenn die Antwort an einen Client Aufruf von [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
Message-Dienste, die eine Service-Eintrag-Funktion exportieren müssen die **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) und **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) Eigenschaften im Abschnitt Dienst Nachricht enthalten. MAPISVC.INF. 
  

