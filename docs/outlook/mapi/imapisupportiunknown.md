---
title: IMAPISupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport
api_type:
- COM
ms.assetid: 92bfe604-18dd-46a1-9ae8-0b04167606bd
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7daa8ec536a81abc196bbb23a0e1a48e826579e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792437"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**Betrifft**: Outlook 
  
Bietet Implementierungen für Aufgaben vorgestellt, die in der Regel vom Dienstanbieter und Nachricht Webdienstfunktionen Entry Point ausgeführt werden. -Dienstanbieter erhalten einen Zeiger auf ihre Support-Objekt, wenn MAPI-ihre Anbieterobjekt Logon-Methode aufrufen. Message-Dienste erhalten den Anruf an ihre Funktion Eintrag Zeiger Objekt Unterstützung.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Verf�gbar gemacht von:  <br/> |Unterstützungsobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPISup  <br/> |
|Zeigertyp:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[GetLastError](imapisupport-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur, die Informationen zu dem Fehler der vorherigen Support-Objekt enthält.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Ruft die Adressen der MAPI-Speicher Reservierung und Freigabe Funktionen ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md)).  <br/> |
|[Abonnieren](imapisupport-subscribe.md) <br/> |Registriert ein Advise-Empfänger Erhalt von Benachrichtigungen über MAPI an.  <br/> |
|[Abonnement kündigen](imapisupport-unsubscribe.md) <br/> |Hebt die Verantwortung für Benachrichtigungen gesendet werden, die zuvor mit einem Aufruf der **Subscribe** -Methode festgelegt wurde.  <br/> |
|[Benachrichtigen](imapisupport-notify.md) <br/> |Sendet eine Benachrichtigung über ein bestimmtes Ereignis mit einer Advise-Datenquelle, die ursprünglich für die Benachrichtigung über die **Subscribe** -Methode registriert.  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Ändert die Statustabelle durch eine neue Zeile hinzufügen oder Ändern einer vorhandenen Zeile.  <br/> |
|["OpenProfileSection"](imapisupport-openprofilesection.md) <br/> |Öffnet einen Abschnitt des aktuellen Profils und gibt einen Zeiger [IProfSect](iprofsectimapiprop.md) für den weiteren Zugriff  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Registriert einen Adressbuchhierarchie Präprozessor-Funktion (eine Funktion, die den [PreprocessMessage](preprocessmessage.md) Prototyp entspricht).  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Erstellt eine neue [MAPIUID](mapiuid.md) -Struktur, die als eindeutiger Bezeichner verwendet werden.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Markiert ein Objekt als nicht mehr verwendet werden.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Bietet Kontrolle über die CPU auf die MAPI-Warteschlange, damit sie alle Aufgaben ausführen kann, notwendig hält.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Benachrichtigt die MAPI-Warteschlange von einer Änderung im Status oder eine Anforderung für den Dienst an.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Erstellt einen Eintrag Bezeichner für eine einmalige Adresse.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Registriert eine **MAPIUID** -Struktur, die den Dienstanbieter eindeutig darstellt.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob sie sich auf dasselbe Objekt verweisen.  <br/> |
|[OpenTemplateID](imapisupport-opentemplateid.md) <br/> |Öffnet einen Empfänger Eintrag in einem fremden Adressbuchanbieter.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Öffnet ein Objekt und gibt einen Schnittstellenzeiger für den weiteren Zugriff.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Gibt einen Zeiger auf die einmaligen MAPI-Tabelle (eine Liste der Vorlagen, dass alle Anbieter für die Unterstützung für das Erstellen von neuen Empfänger Adressbuch).  <br/> |
|[Adresse](imapisupport-address.md) <br/> |Zeigt das Dialogfeld allgemeine Adresse an.  <br/> |
|[Details](imapisupport-details.md) <br/> |Zeigt ein Dialogfeld, das Details zu einem bestimmten Buch Adresseintrag anzeigt.  <br/> |
|[NewEntry](imapisupport-newentry.md) <br/> |Fügt einen neuen Empfänger direkt an einen Adressbuchcontainer oder die Empfängerliste von ausgehenden Nachrichten.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Zeigt eine Konfiguration Eigenschaftenblatt.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Kopiert oder verschiebt Nachrichten aus einem Ordner in einen anderen Ordner.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Kopiert oder Verschiebt einen Ordner von seinem aktuellen übergeordneten Ordner in einer anderen übergeordneten Ordner.  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Kopiert oder verschiebt alle Eigenschaften eines Objekts, mit Ausnahme von speziell Ausgeschlossene Eigenschaften in ein anderes Objekt.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Kopiert oder Verschiebt einen oder mehrere Eigenschaften eines Objekts in ein anderes Objekt.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Ruft ein Fortschritt-Objekt, das eine Statusanzeige wird angezeigt.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Generiert einen Lese- oder nonread Bericht für eine Nachricht.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Bereitet eine Nachricht für die Übermittlung an die MAPI-Warteschlange.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Schließt eine Nachricht Empfängerliste bestimmten Verteilerlisten erweitern.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Verarbeitet eine gesendete Nachricht.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Bietet Zugriff auf das Adressbuch.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Führt Nachbearbeitung für eine Nachricht aus.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Fordert die ordnungsgemäße Version von eines Nachrichtenspeichers.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Bereitstellung und Nondelivery Berichte generiert.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Konvertiert einen Nachrichtenspeicher interne Eintrags-ID auf einen Eintrag Bezeichner MAPI-Standardformat.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Ändert eine Nachricht Profilabschnitt permanent gespeichert.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Zugriff auf einen Datenstrom ein Speicherobjekt implementiert.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Erstellt ein Objekt "Message" Service Support.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Beheben Sie, Bücher, Nachrichtenspeicher, Transportanbieter und Nachricht, dass jede Services eigene Unterstützungsobjekte verfügen. Dienstanbieter und Message-Dienste werden die Methoden in ihre Unterstützungsobjekte im Rahmen der Implementierung von anderen Schnittstellenmethoden aufgerufen. Jedes verschiedene Support-Objekt verfügt über vollständigen Implementierungen der Methoden, die an die aufrufende gelten; die Methoden, die nicht anwendbar sind zurückgeben MAPI_E_NO_SUPPORT. Address Book Anbieter Unterstützungsobjekte haben Implementierungen für die folgenden Methoden:
  
||||
|:-----|:-----|:-----|
|**Adresse** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Details** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**GetLastError** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NewEntry** <br/> |**NewUID** <br/> |
|**Benachrichtigen** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**"OpenProfileSection"** <br/> |**OpenTemplateID** <br/> |**SetProviderUID** <br/> |
|**Abonnieren** <br/> |**Abonnement kündigen** <br/> |**WrapStoreEntryID** <br/> |
   
Nachricht Store Anbieter Unterstützungsobjekte haben Implementierungen für die folgenden Methoden:
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Benachrichtigen** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**"OpenProfileSection"** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Abonnieren** <br/> |**Abonnement kündigen** <br/> |
|**WrapStoreEntryID** <br/> |
   
Transport-Anbieter Unterstützungsobjekte haben Implementierungen für die folgenden Methoden:
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**GetLastError** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Benachrichtigen** <br/> |**"OpenProfileSection"** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Abonnieren** <br/> |**Abonnement kündigen** <br/> |
   
Nachricht Service Unterstützungsobjekte haben Implementierungen für die folgenden Methoden:
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**GetLastError** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**"OpenProfileSection"** <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

