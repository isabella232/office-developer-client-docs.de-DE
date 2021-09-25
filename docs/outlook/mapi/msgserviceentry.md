---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8cfd9e655a9690ac2207a36849fe1b6c63d99719
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575358"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert einen Prototyp für eine Nachrichtendienst-Einstiegspunktfunktion zur Unterstützung der Nachrichtendienstkonfiguration. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Nachrichtendienste  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |MAPI  <br/> |
   
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

 _Hinstance_
  
> [in] Handle der Instanz der Dienstanbieter-DLL. Das Handle wird in der Regel zum Abrufen von Ressourcen verwendet. 
    
 _lpMalloc_
  
> [in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle** verfügbar machen kann. Der Nachrichtendienst muss diese Zuordnungsmethode möglicherweise verwenden, wenn er mit bestimmten Schnittstellen wie **IStream** arbeitet. 
    
 _lpMAPISup_
  
> [in] Zeiger auf eine [IMAPISupport: IUnknown-Schnittstellenimplementierungen.](imapisupportiunknown.md) 
    
 _ulUIParam_
  
> [in] Ein implementierungsspezifischer Wert, der zum Übergeben von Benutzeroberflächeninformationen an eine Funktion oder null verwendet wird. Der  _ulUIParam-Parameter_ ist das übergeordnete Fensterhandle für das Konfigurationsdialogfeld und hat den Typ HWND (umwandeln in eine ULONG_PTR). Der Wert Null gibt an, dass kein übergeordnetes Fenster vorhanden ist. 
    
 _ulFlags_
  
> [in] Bitmaske mit Flags, die Optionen für die Diensteintragsfunktion angeben. Die folgenden Flags können festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> Die Konfigurations-Benutzeroberfläche des Diensts sollte die aktuelle Konfiguration anzeigen, dem Benutzer jedoch nicht erlauben, sie zu ändern. 
    
SERVICE_UI_ALLOWED 
  
> Lässt zu, dass bei Bedarf ein Konfigurationsdialogfeld angezeigt wird. Wenn das SERVICE_UI_ALLOWED Flag festgelegt ist, sollte das Dialogfeld nur angezeigt werden, wenn das Wertarray der  _lpProps-Eigenschaft_ leer ist oder keine gültige Konfiguration enthält. Wenn SERVICE_UI_ALLOWED nicht festgelegt ist, wird möglicherweise weiterhin ein Dialogfeld angezeigt, wenn das SERVICE_UI_ALWAYS-Kennzeichen festgelegt ist. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Fordert an, dass das Konfigurationsdialogfeld für den aktiven Anbieter über anderen Dialogfeldern angezeigt wird. 
    
SERVICE_UI_ALWAYS 
  
> Erfordert, dass der Nachrichtendienst ein Konfigurationsdialogfeld anzeigt. Wenn das SERVICE_UI_ALWAYS Kennzeichen nicht festgelegt ist, wird möglicherweise weiterhin ein Konfigurationsdialogfeld angezeigt, wenn das SERVICE_UI_ALLOWED-Flag festgelegt ist und gültige Konfigurationsinformationen im  _LpProps-Eigenschaftswertarray_ nicht verfügbar sind. Es müssen entweder SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS festgelegt werden, damit eine Benutzeroberfläche angezeigt werden kann. 
    
 _ulContext_
  
> [in] Der Konfigurationsvorgang, den die MAPI derzeit ausführt. Der  _ulContext-Parameter_ enthält einen der folgenden Werte: 
    
MSG_SERVICE_CONFIGURE 
  
> Änderungen an der Konfiguration des Diensts sollten im Profil vorgenommen werden. Wenn das SERVICE_UI_ALWAYS-Kennzeichen festgelegt ist, sollte der Dienst sein Konfigurationsdialogfeld anzeigen. Das Dialogfeld sollte auch angezeigt werden, wenn das flag SERVICE_UI_ALLOWED festgelegt ist und der  _Parameter lpProps_ leer ist oder keine gültigen Konfigurationsdaten enthält. Wenn  _lpProps_ gültige Daten enthält, sollte kein Dialogfeld angezeigt werden, und der Dienst sollte diese Daten verwenden, um die Konfigurationsänderung vorzunehmen. 
    
MSG_SERVICE_CREATE 
  
> Der Dienst wird einem Profil hinzugefügt. Wenn entweder das SERVICE_UI_ALWAYS oder SERVICE_UI_ALLOWED Flag festgelegt ist, sollte der Dienst das Konfigurationsdialogfeld anzeigen. Wenn kein Flag festgelegt ist, sollte der Dienst fehlschlagen. 
    
MSG_SERVICE_DELETE 
  
> Der Dienst wird aus einem Profil entfernt. Nach Erhalt dieses Ereignisses sollte der Dienst S_OK zurückgeben.
    
MSG_SERVICE_INSTALL 
  
> Der Dienst wurde auf der Arbeitsstation des Benutzers über ein Netzwerk, eine Diskette oder ein anderes externes Medium installiert. Nach Erhalt dieses Ereignisses gibt der Dienst in der Regel S_OK zurück. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Fordert an, dass der Dienst eine zusätzliche Instanz eines Anbieters erstellt. Wenn der Dienst diesen Vorgang unterstützt, sollte er [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md)aufrufen. Wenn der Dienst diesen Vorgang nicht unterstützt, kann er MAPI_E_NO_SUPPORT zurückgeben. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Fordert an, dass der Dienst eine Anbieterinstanz löscht. Wenn der Dienst diesen Vorgang unterstützt, sollte er [IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md)aufrufen. Wenn der Dienst diesen Vorgang nicht unterstützt, kann er MAPI_E_NO_SUPPORT zurückgeben.
    
MSG_SERVICE_UNINSTALL 
  
> Der Dienst wird entfernt. Nach Erhalt dieses Ereignisses kann der Dienst alle Bereinigungsaufgaben ausführen, die vor dem Beenden des Diensts durchgeführt werden sollen, und dann mit einem Erfolgswert zurückgegeben werden. Wenn der Benutzer die Entfernung abbricht, sollte der Dienst MAPI_E_USER_CANCEL zurückgeben. 
    
 _cValues_
  
> [in] Anzahl der Eigenschaftswerte im Array, auf das durch den  _LpProps-Parameter_ verwiesen wird. Der Wert des  _cValues-Parameters_ ist Null, wenn mapi keine Eigenschaftswerte übergibt. 
    
 _lpProps_
  
> [in] Zeiger auf ein optionales Array von [SPropValue-Strukturen,](spropvalue.md) das Werte für vom Anbieter unterstützte Eigenschaften angibt, die die Funktion zum Konfigurieren des Nachrichtendiensts verwendet. Die Funktion verwendet diesen Parameter nur, wenn der  _ulContext-Parameter_ auf MSG_SERVICE_CONFIGURE festgelegt ist. Dieser Parameter wird häufig verwendet, um den Pfad zu einer Datei für einen dateibasierten Dienst zu übergeben, z. B. einen persönlichen Adressbuchdienst. Wenn das MSG_SERVICE_CONFIGURE-Flag nicht im  _ulFlags-Parameter_ übergeben wird, muss der  _LpProps-Parameter_ Null sein. 
    
 _lpProviderAdmin_
  
> [in] Zeiger auf eine [IProviderAdmin:IUnknown-Schnittstelle,](iprovideradminiunknown.md) mit der die Funktion Profilabschnitte für einen bestimmten Anbieter im aktuellen Nachrichtendienst suchen kann. 
    
 _lppMapiError_
  
> [out] Zeiger auf eine [MAPIERROR-Struktur.](mapierror.md) Die Struktur wird mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) zugeordnet. Alle Member sind optional, obwohl die meisten Strukturen eine gültige Fehlermeldungszeichenfolge im  _lpszError-Element_ enthalten. Wenn die  _lpszComponent-_ oder  _lpszError-Elemente_ der Struktur vorhanden sind, muss ihr Speicher schließlich durch einen einzigen Aufruf von [MAPIFreeBuffer](mapifreebuffer.md) in der Basisstruktur freigegeben werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_UNCONFIGURED 
  
> Der Dienstanbieter wurde nicht konfiguriert. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
MAPI_E_NO_SUPPORT 
  
> Der Anbieter unterstützt entweder keine Änderungen an seinen Objekten oder keine Benachrichtigung über Änderungen. 
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine Funktion, die mit dem Prototyp der **MSGSERVICEENTRY-Funktion** definiert wurde, ermöglicht es Nachrichtendiensten, sich selbst zu konfigurieren oder andere dienstspezifische Aktionen auszuführen. Die Funktion stellt in erster Linie ein Dialogfeld bereit, in dem der Benutzer für den Nachrichtendienst spezifische Einstellungen ändern kann. Sie kann auch die programmgesteuerte Konfiguration mithilfe des Eigenschaftswertarrays unterstützen, das im  _LpProps-Parameter_ übergeben wird. Die programmgesteuerte Konfiguration ist optional, es sei denn, der Dienst unterstützt den Profil-Assistenten, für den er erforderlich ist. 
  
MAPI ruft diesen Einstiegspunkt aus der Systemsteuerungsanwendung oder als Reaktion auf eine Clientanwendung auf, die [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) oder [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)aufruft. 
  
MAPI legt keine Einschränkung für den Funktionsnamen fest, den ein Nachrichtendienst für den **MSGSERVICEENTRY-Prototyp** verwendet, bevorzugt jedoch den Namen **ServiceEntry.** Es gibt keine Einschränkung der Ordnungszahl für die Funktion, und eine einzelne Anbieter-DLL kann mehr als eine Funktion enthalten. Es kann jedoch nur eine der Funktionen den Namen **ServiceEntry** haben. 
  
Ein Nachrichtendienst kann die [BuildDisplayTable-Funktion](builddisplaytable.md) und die [IMAPISupport::D oConfigPropsheet-Methode](imapisupport-doconfigpropsheet.md) verwenden, um die Implementierung des Konfigurationsdialogfelds zu vereinfachen. 
  
Es ist möglich, dass ein Benutzer einen MSG_SERVICE_UNINSTALL Vorgang abbricht. In diesem Fall sollte die **ServiceEntry-Funktion** mit dem Benutzer überprüfen, ob der Dienst nicht entfernt werden soll, und MAPI_E_USER_CANCEL zurückgeben, wenn der Dienst installiert bleibt. 
  
Eine auf dem **MSGSERVICEENTRY-Prototyp** basierende Funktion gibt einen der aufgelisteten HRESULT-Werte zurück. MAPI leitet diesen Wert weiter, wenn sie auf den Aufruf eines Clients an [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)antwortet. 
  
Nachrichtendienste, die eine Diensteintragsfunktion exportieren, müssen die Eigenschaften **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) und **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) im Nachrichtendienstabschnitt von MAPISVC.INF enthalten. 
  

