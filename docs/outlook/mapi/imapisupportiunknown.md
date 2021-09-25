---
title: IMAPISupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport
api_type:
- COM
ms.assetid: 92bfe604-18dd-46a1-9ae8-0b04167606bd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1ad54ca8efccebd28ed38ebd457fb258a3f59790
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625392"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Implementierungen für Aufgaben bereit, die in der Regel von Dienstanbietern und Nachrichtendienst-Einstiegspunktfunktionen ausgeführt werden. Dienstanbieter erhalten einen Zeiger auf ihr Supportobjekt, wenn MAPI die Anmeldemethode des Anbieterobjekts aufruft. Nachrichtendienste erhalten ihren Unterstützungsobjektzeiger im Aufruf ihrer Einstiegspunktfunktion.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Supportobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPISup  <br/> |
|Zeigertyp:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>VTable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterror](imapisupport-getlasterror.md) <br/> |Gibt eine [MAPIERROR-Struktur](mapierror.md) zurück, die Informationen zum vorherigen Supportobjektfehler enthält.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Ruft die Adressen der MAPI-Speicherzuweisung und der Zuordnungsfunktionen ab ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md)).  <br/> |
|[Abonnieren](imapisupport-subscribe.md) <br/> |Registriert eine Empfehlungssenke, um Benachrichtigungen über MAPI zu erhalten.  <br/> |
|[Unsubscribe](imapisupport-unsubscribe.md) <br/> |Bricht die Verantwortung für das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **Subscribe-Methode** eingerichtet wurde.  <br/> |
|[Notify](imapisupport-notify.md) <br/> |Sendet eine Benachrichtigung über ein angegebenes Ereignis an eine Empfehlungsquelle, die ursprünglich über die **Subscribe-Methode** für die Benachrichtigung registriert wurde.  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Ändert die Statustabelle, indem eine neue Zeile hinzugefügt oder eine vorhandene Zeile geändert wird.  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect-Zeiger](iprofsectimapiprop.md) für weiteren Zugriff zurück.  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Registriert die Präprozessorfunktion eines Transportanbieters (eine Funktion, die dem [PreprocessMessage-Prototyp](preprocessmessage.md) entspricht).  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Erstellt eine neue [MAPIUID-Struktur,](mapiuid.md) die als eindeutiger Bezeichner verwendet werden soll.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Markiert ein Objekt als nicht verwendbar.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Gibt die Steuerung der CPU an den MAPI-Spooler weiter, damit alle aufgaben ausgeführt werden können, die er für erforderlich hält.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Benachrichtigt den MAPI-Spooler über eine Statusänderung oder eine Dienstanforderung.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Erstellt einen Eintragsbezeichner für eine einmalige Adresse.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Registriert eine **MAPIUID-Struktur,** die den Dienstanbieter eindeutig darstellt.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie auf dasselbe Objekt verweisen.  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Öffnet einen Empfängereintrag in einem fremden Adressbuchanbieter.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Öffnet ein Objekt und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Gibt einen Zeiger auf die EINMALIGE MAPI-Tabelle zurück (eine Liste der Vorlagen, die alle Adressbuchanbieter beim Erstellen neuer Empfänger unterstützen).  <br/> |
|[Adresse](imapisupport-address.md) <br/> |Zeigt das allgemeine Adressdialogfeld an.  <br/> |
|[Details](imapisupport-details.md) <br/> |Zeigt ein Dialogfeld an, in dem Details zu einem bestimmten Adressbucheintrag angezeigt werden.  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |Fügt einen neuen Empfänger direkt zu einem Adressbuchcontainer oder zur Empfängerliste einer ausgehenden Nachricht hinzu.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Zeigt ein Konfigurationseigenschaftenblatt an.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Kopiert oder verschiebt Nachrichten von einem Ordner in einen anderen Ordner.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Kopiert oder verschiebt einen Ordner aus seinem aktuellen übergeordneten Ordner in einen anderen übergeordneten Ordner.  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Kopiert oder verschiebt alle Eigenschaften eines Objekts, mit Ausnahme ausdrücklich ausgeschlossener Eigenschaften, in ein anderes Objekt.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Kopiert oder verschiebt eine oder mehrere Eigenschaften eines Objekts in ein anderes Objekt.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Ruft ein Statusobjekt ab, das eine Statusanzeige anzeigt.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Generiert einen gelesenen oder nicht gelesenen Bericht für eine Nachricht.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Bereitet eine Nachricht für die Übermittlung an den MAPI-Spooler vor.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Schließt die Empfängerliste einer Nachricht ab und erweitert bestimmte Verteilerlisten.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Verarbeitet eine gesendete Nachricht.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Ermöglicht den Zugriff auf das Adressbuch.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Führt eine Nachverarbeitung für eine Nachricht aus.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Fordert die geordnete Veröffentlichung eines Nachrichtenspeichers an.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Generiert Übermittlungs- und Unzustellbarkeitsberichte.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Konvertiert den internen Eintragsbezeichner eines Nachrichtenspeichers in einen Eintragsbezeichner im MAPI-Standardformat.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Nimmt Änderungen an einem Nachrichtenspeicherprofilabschnitt dauerhaft vor.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Implementiert ein Speicherobjekt für den Zugriff auf einen Datenstrom.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Erstellt ein Nachrichtendienst-Supportobjekt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Adressbücher, Nachrichtenspeicher, Transportanbieter und Nachrichtendienste verfügen jeweils über eigene Supportobjekte. Dienstanbieter und Nachrichtendienste rufen die Methoden in ihren Supportobjekten als Teil ihrer Implementierungen anderer Schnittstellenmethoden auf. Jedes unterschiedliche Unterstützungsobjekt verfügt über vollständige Implementierungen der Methoden, die für den Aufrufer gelten. die methoden, die nicht anwendbar sind, geben MAPI_E_NO_SUPPORT zurück. Supportobjekte für Adressbuchanbieter verfügen über Implementierungen für die folgenden Methoden:
  
||||
|:-----|:-----|:-----|
|**Adresse** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Details** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**Getlasterror** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Abonnieren** <br/> |**Unsubscribe** <br/> |**WrapStoreEntryID** <br/> |
   
Supportobjekte des Nachrichtenspeicheranbieters verfügen über Implementierungen für die folgenden Methoden:
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**Getlasterror** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Notify** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Abonnieren** <br/> |**Unsubscribe** <br/> |
|**WrapStoreEntryID** <br/> |
   
Transport provider support objects have implementations for the following methods:
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**Getlasterror** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Notify** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Abonnieren** <br/> |**Unsubscribe** <br/> |
   
Nachrichtendienst-Supportobjekte verfügen über Implementierungen für die folgenden Methoden:
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**Getlasterror** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

