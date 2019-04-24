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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341608"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert einen Prototyp für eine Nachrichtendienst-Einstiegspunktfunktion zur Unterstützung der Nachrichtendienst Konfiguration. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |Nachrichtendienste  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |MAPI  <br/> |
   
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
  
> in Handle der Instanz des Diensts providerDLL. Das Handle wird in der Regel zum Abrufen von Ressourcen verwendet. 
    
 _lpMalloc_
  
> in Zeiger auf ein Speicher Reservierungs Objekt, das die OLE **IMalloc** -Schnittstelle verfügbar macht. Möglicherweise muss der Nachrichtendienst diese Zuordnungsmethode beim Arbeiten mit bestimmten Schnittstellen wie **IStream**verwenden. 
    
 _lpMAPISup_
  
> in Zeiger auf eine [IMAPISupport: IUnknown](imapisupportiunknown.md) -Schnittstellenimplementierung. 
    
 _ulUIParam_
  
> in Ein implementierungsspezifischer Wert, der zum Übergeben von Benutzeroberflächeninformationen an eine Funktion oder NULL verwendet wird. Der _ulUIParam_ -Parameter ist das übergeordnete Fensterhandle für das Konfigurationsdialogfeld und vom Typ HWND (Umwandlung in einen ULONG_PTR). Der Wert 0 (null) gibt an, dass kein übergeordnetes Fenster vorhanden ist. 
    
 _ulFlags_
  
> in Bitmaske von Flags, die Optionen für die Dienst Eingabefunktion angeben. Die folgenden Flags können festgelegt werden:
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> Die Benutzeroberfläche der Konfiguration des Diensts sollte die aktuelle Konfiguration anzeigen, aber nicht zulassen, dass der Benutzer Sie ändern kann. 
    
SERVICE_UI_ALLOWED 
  
> Ermöglicht bei Bedarf ein Konfigurationsdialogfeld. Wenn das SERVICE_UI_ALLOWED-Flag festgelegt ist, sollte das Dialogfeld nur angezeigt werden, wenn das _lpProps_ -Eigenschaftswert-Array leer ist oder keine gültige Konfiguration enthält. Wenn SERVICE_UI_ALLOWED nicht festgelegt ist, wird möglicherweise weiterhin ein Dialogfeld angezeigt, wenn das SERVICE_UI_ALWAYS-Flag festgelegt ist. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Fordert, dass das Konfigurationsdialogfeld für den aktiven Anbieter über den anderen Dialogfeldern angezeigt wird. 
    
SERVICE_UI_ALWAYS 
  
> Erfordert, dass der Nachrichtendienst ein Konfigurationsdialogfeld anzeigt. Wenn das SERVICE_UI_ALWAYS-Flag nicht festgelegt ist, wird möglicherweise weiterhin ein Konfigurationsdialogfeld angezeigt, wenn das SERVICE_UI_ALLOWED-Flag festgelegt ist und gültige Konfigurationsinformationen aus dem _lpProps_ -Eigenschaftswert Array nicht verfügbar sind. Entweder SERVICE_UI_ALLOWED oder SERVICE_UI_ALWAYS muss festgelegt werden, damit eine Benutzeroberfläche angezeigt werden kann. 
    
 _ulContext_
  
> in Der Konfigurationsvorgang, den MAPI derzeit ausführt. Der _ulContext_ -Parameter enthält einen der folgenden Werte: 
    
MSG_SERVICE_CONFIGURE 
  
> Änderungen an der Konfiguration des Diensts sollten im Profil vorgenommen werden. Wenn das SERVICE_UI_ALWAYS-Flag festgelegt ist, sollte der Dienst sein Konfigurationsdialogfeld anzeigen. Das Dialogfeld sollte auch angezeigt werden, wenn das SERVICE_UI_ALLOWED-Flag festgelegt ist und der Parameter _lpProps_ leer ist oder keine gültigen Konfigurationsdaten enthält. Wenn _lpProps_ gültige Daten enthält, sollte kein Dialogfeld angezeigt werden, und der Dienst sollte diese Daten zum vornehmen der Konfigurationsänderung verwenden. 
    
MSG_SERVICE_CREATE 
  
> Der Dienst wird einem Profil hinzugefügt. Wenn entweder das SERVICE_UI_ALWAYS-oder das SERVICE_UI_ALLOWED-Flag festgelegt ist, sollte der Dienst sein Konfigurationsdialogfeld anzeigen. Wenn kein Flag festgelegt ist, sollte der Dienst einen Fehler verursachen. 
    
MSG_SERVICE_DELETE 
  
> Der Dienst wird aus einem Profil entfernt. Nach dem Empfang dieses Ereignisses sollte der Dienst S_OK zurückgeben.
    
MSG_SERVICE_INSTALL 
  
> Der Dienst wurde von einem Netzwerk, einer Diskette oder einem anderen externen Medium auf der Arbeitsstation des Benutzers installiert. Nach dem Empfang dieses Ereignisses gibt der Dienst in der Regel S_OK zurück. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Fordert, dass der Dienst eine zusätzliche Instanz eines Anbieters erstellt. Wenn der Dienst diesen Vorgang unterstützt, sollte er [IProviderAdmin:: CreateProvider](iprovideradmin-createprovider.md)aufrufen. Wenn der Dienst diesen Vorgang nicht unterstützt, kann er MAPI_E_NO_SUPPORT zurückgeben. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Fordert, dass der Dienst eine Anbieterinstanz löscht. Wenn der Dienst diesen Vorgang unterstützt, sollte er [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md)aufrufen. Wenn der Dienst diesen Vorgang nicht unterstützt, kann er MAPI_E_NO_SUPPORT zurückgeben.
    
MSG_SERVICE_UNINSTALL 
  
> Der Dienst wird entfernt. Nach dem Empfang dieses Ereignisses kann der Dienst alle Bereinigungsaufgaben ausführen, die vor dem Beenden des Diensts ausgeführt werden sollten und dann mit einem Erfolgswert zurückgegeben werden. Wenn der Benutzer das Entfernen abbricht, sollte der Dienst MAPI_E_USER_CANCEL zurückgeben. 
    
 _cValues_
  
> in Die Anzahl der Eigenschaftswerte im Array, auf die durch den _lpProps_ -Parameter verwiesen wird. Der Wert des _cValues_ -Parameters ist NULL, wenn MAPI keine Eigenschaftswerte übergibt. 
    
 _lpProps_
  
> in Zeiger auf ein optionales Array von [SPropValue](spropvalue.md) -Strukturen, die Werte für Anbieter gestützte Eigenschaften angeben, die die Funktion beim Konfigurieren des Nachrichtendiensts verwendet. Die Funktion verwendet diesen Parameter nur, wenn der _ulContext_ -Parameter auf MSG_SERVICE_CONFIGURE festgelegt ist. Dieser Parameter wird in der Regel verwendet, um den Pfad an eine Datei für einen dateibasierten Dienst, beispielsweise einen persönlichen Adressbuchdienst, zu übergeben. Wenn das MSG_SERVICE_CONFIGURE-Flag nicht im _ulFlags_ -Parameter übergeben wird, muss der _lpProps_ -Parameter NULL sein. 
    
 _lpProviderAdmin_
  
> in Zeiger auf eine [IProviderAdmin: IUnknown](iprovideradminiunknown.md) -Schnittstelle, die die Funktion verwenden kann, um Profilabschnitte für einen bestimmten Anbieter im aktuellen Nachrichtendienst zu suchen. 
    
 _lppMapiError_
  
> Out Zeiger auf eine [MAPIERROR](mapierror.md) -Struktur. Die Struktur wird mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion zugeordnet. Alle Member sind optional, obwohl die meisten Strukturen eine gültige Fehlermeldungszeichenfolge im _lpszError_ -Element enthalten. Wenn die _lpszComponent_ -oder _lpszError_ -Member der Struktur vorhanden sind, muss Ihr Arbeitsspeicher schließlich durch einen einzelnen Aufruf von [mapifreebufferfreigegeben](mapifreebuffer.md) in der Basisstruktur freigegeben werden. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_UNCONFIGURED 
  
> Der Dienstanbieter wurde nicht konfiguriert. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat. 
    
MAPI_E_NO_SUPPORT 
  
> Der Anbieter unterstützt entweder keine Änderungen an seinen Objekten oder unterstützt keine Benachrichtigung über Änderungen. 
    
MAPI_E_BAD_CHARWIDTH 
  
> Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.
    
## <a name="remarks"></a>Bemerkungen

Eine mit dem **MSGSERVICEENTRY** -Funktionsprototyp definierte Funktion ermöglicht es Nachrichtendiensten, sich selbst zu konfigurieren oder andere dienstspezifische Aktionen auszuführen. Die Funktion liefert in erster Linie ein Dialogfeld, in dem der Benutzer die Einstellungen für den Nachrichtendienst ändern kann. Die programmgesteuerte Konfiguration kann auch mithilfe des Eigenschafts Wertarrays unterstützt werden, das im _lpProps_ -Parameter übergeben wird. Die programmgesteuerte Konfiguration ist optional, es sei denn, der Dienst unterstützt den Profil-Assistenten, für den er erforderlich ist. 
  
MAPI ruft diesen Einstiegspunkt aus der Systemsteuerungsanwendung oder als Reaktion auf eine Clientanwendung auf, die [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) oder [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)aufruft. 
  
MAPI gibt keine Einschränkung für den Funktionsnamen, den ein Nachrichtendienst für den **MSGSERVICEENTRY** -Prototyp verwendet, aber bevorzugt den Namen **ServiceEntry**. Es gibt keine Beschränkung für die Ordnungszahl für die Funktion, und eine einzelne Anbieter-DLL kann mehr als eine Funktion enthalten. Es kann jedoch nur eine der Funktionen mit dem Namen **ServiceEntry**. 
  
Ein Nachrichtendienst kann die [BuildDisplayTable](builddisplaytable.md) -Funktion und die [IMAPISupport::D-oconfigpropsheet](imapisupport-doconfigpropsheet.md) -Methode verwenden, um die Implementierung der Konfigurationsdialogfelder zu vereinfachen. 
  
Ein Benutzer kann einen MSG_SERVICE_UNINSTALL-Vorgang abbrechen. In diesem Fall sollte die **ServiceEntry** -Funktion mit dem Benutzer überprüfen, ob der Dienst nicht entfernt werden soll, und MAPI_E_USER_CANCEL zurückgeben, wenn der Dienst installiert bleibt. 
  
Eine auf dem **MSGSERVICEENTRY** -Prototyp basierende Funktion gibt einen der aufgeführten HRESULT-Werte zurück. MAPI leitet diesen Wert weiter, wenn er auf den Aufruf eines Clients an [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)reagiert. 
  
Nachrichtendienste, die eine Diensteintrags Funktion exportieren, müssen die Eigenschaften **PR_SERVICE_DLL_NAME** ([Pidtagservicedllname (](pidtagservicedllname-canonical-property.md)) und **PR_SERVICE_ENTRY_NAME** ([pidtagserviceentryname (](pidtagserviceentryname-canonical-property.md)) im Abschnitt Nachrichtendienst MAPISVC. INF. 
  

