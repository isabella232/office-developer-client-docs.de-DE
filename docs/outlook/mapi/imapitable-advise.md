---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: cd6b119bd88fccf80bf2488592a24b3398e6e8af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594243"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Registriert ein Empfängerobjekt Advise, um die Benachrichtigung der Auswirkungen auf die Tabelle angegebenen Ereignisse.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Parameter

 _ulEventMask_
  
> [in] Wert, der den Typ des Ereignisses, das die Benachrichtigung generiert wird. Nur der folgende Wert ist gültig:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [in] Zeiger auf eine Advise-Empfängerobjekt nachfolgenden Benachrichtigungen zu empfangen. Diese Advise-Empfängerobjekt muss bereits zugewiesen wurden.
    
 _lpulConnection_
  
> [out] Zeiger auf einen Wert ungleich NULL, der die erfolgreiche benachrichtigungsregistrierung darstellt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die benachrichtigungsregistrierung erfolgreich abgeschlossen.
    
MAPI_E_NO_SUPPORT 
  
> Die Tabelle-Implementierung unterstützt keine Änderungen auf die Zeilen und Spalten, oder unterstützt keine Benachrichtigung.
    
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie die **IMAPITable::Advise** -Methode, um ein Table-Objekt im Anbieter für Benachrichtigung Rückrufe implementiert registrieren. Bei eine Änderung an das Table-Objekt, überprüft der Anbieter finden Sie unter welche Ereignis Maskenbit im _UlEventMask_ -Parameter festgelegt wurde, und daher, welche Art der Änderung. Wenn ein bit festgelegt ist, ruft der Anbieter die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für die Advise-Empfängerobjekt durch den Parameter _LpAdviseSink_ Sie das Ereignis melden angegeben. Daten, die in der Benachrichtigungsstruktur der **OnNotify** Routine übergeben wird das Ereignis beschrieben. 
  
Der Aufruf von **OnNotify** kann auftreten, während des Anrufs, der das Objekt ändert oder folgenden jederzeit. Auf Systemen, die mehreren Threads der Ausführung zu unterstützen, kann der Aufruf von **OnNotify** auf einem beliebigen Thread auftreten. Für eine Möglichkeit, einen Anruf an **OnNotify** aktivieren, die zu einem ungünstigen Zeitpunkt in eine auftreten können, die zum Verarbeiten von sicherer ist, sollte ein Anbieter für die [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) -Funktion verwenden. 
  
Um Benachrichtigungen zu ermöglichen, beraten die Anbieter implementieren **Advise** muss eine Kopie des Zeigers auf die _LpAdviseSink_ Empfängerobjekt; Hierzu wird die **IUnknown:: AddRef** -Methode für die Advise-Empfänger, dessen Objektzeiger verwalten, bis benachrichtigungsregistrierung mit einem Aufruf der Methode [IMAPITable::Unadvise](imapitable-unadvise.md) abgebrochen wird. Die **Advise** -Implementierung sollte weisen eine Verbindungsnummer zu der benachrichtigungsregistrierung und rufen **AddRef** für diese Verbindungsnummer vor der Rückgabe im _LpulConnection_ -Parameter. Dienstanbieter können das Empfängerobjekt Advise freigeben, bevor die Registrierung wird abgebrochen, aber sie nicht, bis die Nummer freigeben müssen ** Unadvise ** aufgerufen wurde. 
  
Nach ein Aufruf von **Advise** erfolgreich abgeschlossen wurde und bevor ** Unadvise ** wurde aufgerufen, Clients müssen bereiten Sie für das Empfängerobjekt Advise freigegeben werden muss. Ein Client sollte daher seine Advise-Empfängerobjekt freigeben, nachdem **Advise** zurückgegeben, wenn es eine bestimmte langfristige Verwendung verfügt. 
  
Aufgrund der asynchronen Verhalten der Benachrichtigung erhalten Implementierungen integrieren, die Tabelle spalteneinstellungen ändern Benachrichtigungen mit Informationen in einer vorherigen Spaltenreihenfolge angeordnet sind. Beispielsweise könnte eine Tabellenzeile für eine Nachricht zurückgegeben werden, die nur aus dem Container gelöscht wurde. Wenn die Änderung der Einstellung wurde, und Informationen gesendet, aber die Benachrichtigung Tabellenansicht mit diesen Informationen noch nicht aktualisiert wurde, wird eine solche Benachrichtigung gesendet.
  
Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md). Spezifische Informationen zur Tabelle Benachrichtigung finden Sie unter [Zur Tabelle Benachrichtigungen](about-table-notifications.md). Informationen zur Verwendung der Methods **IMAPISupport** zum Benachrichtigung zu unterstützen finden Sie unter [Event Notification unterstützen](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI (engl.) verwendet die **IMAPITable::Advise** -Methode, um für Benachrichtigungen der Tabellenansicht auf dem neuesten Stand zu registrieren.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

