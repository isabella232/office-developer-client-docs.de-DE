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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6da488408d3be9464d6ae1e016d5095707d451e4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415439"
---
# <a name="imapisupport--iunknown"></a>IMAPISupport : IUnknown

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Stellt Implementierungen für Aufgaben bereit, die normalerweise von Dienstanbietern und Nachrichtendienst-Einstiegspunktfunktionen ausgeführt werden. Dienstanbieter erhalten einen Zeiger auf Ihr Support Objekt, wenn MAPI die Anmeldemethode des Anbieterobjekts aufruft. Nachrichtendienste erhalten Ihren Support Objektzeiger im Aufruf ihrer Einstiegspunktfunktion.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi. h  <br/> |
|Verf�gbar gemacht von:  <br/> |Unterstützungsobjekte  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Dienstanbieter  <br/> |
|Schnittstellenbezeichner:  <br/> |IID_IMAPISup  <br/> |
|Zeigertyp:  <br/> |LPMAPISUP  <br/> |
   
## <a name="vtable-order"></a>Vtable-Reihenfolge

|||
|:-----|:-----|
|[Getlasterroraufzurufen](imapisupport-getlasterror.md) <br/> |Gibt eine [MAPIERROR](mapierror.md) -Struktur zurück, die Informationen zum vorherigen Support Objekt Fehler enthält.  <br/> |
|[GetMemAllocRoutines](imapisupport-getmemallocroutines.md) <br/> |Ruft die Adressen der MAPI-Speicher Zuweisungs-und-Zuordnungsfunktionen ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [mapifreebufferfreigegeben](mapifreebuffer.md)) ab.  <br/> |
|[Abonnieren](imapisupport-subscribe.md) <br/> |Registriert eine Advise-Senke, um Benachrichtigungen über MAPI zu empfangen.  <br/> |
|[Unsubscribe](imapisupport-unsubscribe.md) <br/> |Bricht die Verantwortung für das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der **subscribe** -Methode eingerichtet wurden.  <br/> |
|[Benachrichtigen](imapisupport-notify.md) <br/> |Sendet eine Benachrichtigung über ein angegebenes Ereignis an eine Advise-Quelle, die ursprünglich für die Benachrichtigung über die **subscribe** -Methode registriert wurde.  <br/> |
|[ModifyStatusRow](imapisupport-modifystatusrow.md) <br/> |Ändert die Statustabelle, indem eine neue Zeile hinzugefügt oder eine vorhandene Zeile geändert wird.  <br/> |
|[OpenProfileSection](imapisupport-openprofilesection.md) <br/> |Öffnet einen Abschnitt des aktuellen Profils und gibt einen [IProfSect](iprofsectimapiprop.md) -Zeiger für den weiteren Zugriff zurück.  <br/> |
|[RegisterPreprocessor](imapisupport-registerpreprocessor.md) <br/> |Registriert die präprozessorfunktion eines Transportanbieters (eine Funktion, die dem [PreprocessMessage](preprocessmessage.md) -Prototyp entspricht).  <br/> |
|[NewUID](imapisupport-newuid.md) <br/> |Erstellt eine neue [MAPIUID](mapiuid.md) -Struktur, die als eindeutiger Bezeichner verwendet werden soll.  <br/> |
|[MakeInvalid](imapisupport-makeinvalid.md) <br/> |Markiert ein Objekt als unbrauchbar.  <br/> |
|[SpoolerYield](imapisupport-spooleryield.md) <br/> |Gibt die CPU-Steuerung für den MAPI-Spooler an, sodass Sie alle für erforderlich erachteten Aufgaben ausführen kann.  <br/> |
|[SpoolerNotify](imapisupport-spoolernotify.md) <br/> |Benachrichtigt den MAPI-Spooler über eine Änderung des Status oder eine Anforderung für Dienst.  <br/> |
|[CreateOneOff](imapisupport-createoneoff.md) <br/> |Erstellt eine Eintrags-ID für eine einmalige Adresse.  <br/> |
|[SetProviderUID](imapisupport-setprovideruid.md) <br/> |Registriert eine **MAPIUID** -Struktur, die den Dienstanbieter eindeutig darstellt.  <br/> |
|[CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Vergleicht zwei Eintragsbezeichner, um zu bestimmen, ob Sie auf dasselbe Objekt verweisen.  <br/> |
|[OpenTemplate-Nr.](imapisupport-opentemplateid.md) <br/> |Öffnet einen Empfängereintrag in einem fremden Adressbuchanbieter.  <br/> |
|[OpenEntry](imapisupport-openentry.md) <br/> |Öffnet ein Objekt und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.  <br/> |
|[GetOneOffTable](imapisupport-getoneofftable.md) <br/> |Gibt einen Zeiger auf die MAPI-einmalige Tabelle zurück (eine Liste von Vorlagen, die von allen Adressbuch Anbietern für das Erstellen neuer Empfänger unterstützt werden).  <br/> |
|[Adresse](imapisupport-address.md) <br/> |Zeigt das Dialogfeld Allgemeine Adresse an.  <br/> |
|[Details](imapisupport-details.md) <br/> |Zeigt ein Dialogfeld an, in dem Details zu einem bestimmten Adressbucheintrag angezeigt werden.  <br/> |
|[NeuEintrag](imapisupport-newentry.md) <br/> |Fügt einen neuen Empfänger direkt einem Adressbuchcontainer oder der Empfängerliste einer ausgehenden Nachricht hinzu.  <br/> |
|[DoConfigPropsheet](imapisupport-doconfigpropsheet.md) <br/> |Zeigt ein Konfigurationseigenschaften Fenster an.  <br/> |
|[CopyMessages](imapisupport-copymessages.md) <br/> |Kopiert oder verschiebt Nachrichten aus einem Ordner in einen anderen Ordner.  <br/> |
|[CopyFolder](imapisupport-copyfolder.md) <br/> |Kopiert oder verschiebt einen Ordner aus dem aktuellen übergeordneten Ordner in einen anderen übergeordneten Ordner.  <br/> |
|[DoCopyTo](imapisupport-docopyto.md) <br/> |Kopiert oder verschiebt alle Eigenschaften eines Objekts, mit Ausnahme der explizit ausgeschlossenen Eigenschaften, in ein anderes Objekt.  <br/> |
|[DoCopyProps](imapisupport-docopyprops.md) <br/> |Kopiert oder verschiebt eine oder mehrere Eigenschaften eines Objekts in ein anderes Objekt.  <br/> |
|[DoProgressDialog](imapisupport-doprogressdialog.md) <br/> |Ruft ein Progress-Objekt ab, das eine Statusanzeige anzeigt.  <br/> |
|[ReadReceipt](imapisupport-readreceipt.md) <br/> |Generiert einen Lese-oder nicht gelesenen Bericht für eine Nachricht.  <br/> |
|[PrepareSubmit](imapisupport-preparesubmit.md) <br/> |Bereitet eine Nachricht für die Übermittlung an den MAPI-Spooler vor.  <br/> |
|[ExpandRecips](imapisupport-expandrecips.md) <br/> |Vervollständigt die Empfängerliste einer Nachricht und erweitert bestimmte Verteilerlisten.  <br/> |
|[DoSentMail](imapisupport-dosentmail.md) <br/> |Verarbeitet eine gesendete Nachricht.  <br/> |
|[OpenAddressBook](imapisupport-openaddressbook.md) <br/> |Ermöglicht den Zugriff auf das Adressbuch.  <br/> |
|[CompleteMsg](imapisupport-completemsg.md) <br/> |Führt die Nachbearbeitung für eine Nachricht aus.  <br/> |
|[StoreLogoffTransports](imapisupport-storelogofftransports.md) <br/> |Fordert die ordnungsgemäße Freigabe eines Nachrichtenspeichers an.  <br/> |
|[StatusRecips](imapisupport-statusrecips.md) <br/> |Generiert Unzustellbarkeitsberichte.  <br/> |
|[WrapStoreEntryID](imapisupport-wrapstoreentryid.md) <br/> |Konvertiert die interne Eintrags-ID eines Nachrichtenspeichers in eine Eintrags-ID im MAPI-Standardformat.  <br/> |
|[ModifyProfile](imapisupport-modifyprofile.md) <br/> |Änderungen an einem Abschnitt des Nachrichtenspeicher Profils bleiben permanent.  <br/> |
|[IStorageFromStream](imapisupport-istoragefromstream.md) <br/> |Implementiert ein Storage-Objekt, um auf einen Stream zuzugreifen.  <br/> |
|[GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) <br/> |Erstellt ein Support Objekt für den Nachrichtendienst.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Adressbücher, Nachrichtenspeicher, Transportanbieter und Nachrichtendienste verfügen jeweils über eigene Support Objekte. Dienstanbieter und Nachrichtendienste rufen die Methoden in Ihren Support-Objekten als Teil ihrer Implementierungen anderer Schnittstellenmethoden auf. Jedes unterschiedliche Unterstützungsobjekt verfügt über vollständige Implementierungen der Methoden, die für den Aufrufer gelten. die Methoden, die nicht anwendbar sind, geben MAPI_E_NO_SUPPORT zurück. Adressbuchanbieter-Support Objekte verfügen über Implementierungen für die folgenden Methoden:
  
||||
|:-----|:-----|:-----|
|**Adresse** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**Details** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**Getlasterroraufzurufen** <br/> |**GetMemAllocRoutines** <br/> |**GetOneOffTable** <br/> |
|**IStorageFromStream** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**ModifyStatusRow** <br/> |**NeuEintrag** <br/> |**NewUID** <br/> |
|**Benachrichtigen** <br/> |**OpenAddressBook** <br/> |**OpenEntry** <br/> |
|**OpenProfileSection** <br/> |**OpenTemplate-Nr.** <br/> |**SetProviderUID** <br/> |
|**Abonnieren** <br/> |**Unsubscribe** <br/> |**WrapStoreEntryID** <br/> |
   
Nachrichtenspeicher Anbieter-Support Objekte verfügen über Implementierungen für die folgenden Methoden:
  
||||
|:-----|:-----|:-----|
|**CompareEntryIDs** <br/> |**CompleteMsg** <br/> |**CopyFolder** <br/> |
|**CopyMessages** <br/> |**CreateOneOff** <br/> |**DoCopyProps** <br/> |
|**DoCopyTo** <br/> |**DoConfigPropsheet** <br/> |**DoProgressDialog** <br/> |
|**DoSentMail** <br/> |**ExpandRecips** <br/> |**Getlasterroraufzurufen** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**MakeInvalid** <br/> |
|**IStorageFromStream** <br/> |**ModifyProfile** <br/> |**ModifyStatusRow** <br/> |
|**NewUID** <br/> |**Benachrichtigen** <br/> |**OpenAddressBook** <br/> |
|**OpenEntry** <br/> |**OpenProfileSection** <br/> |**PrepareSubmit** <br/> |
|**ReadReceipt** <br/> |**SetProviderUID** <br/> |**SpoolerNotify** <br/> |
|**StoreLogoffTransports** <br/> |**Abonnieren** <br/> |**Unsubscribe** <br/> |
|**WrapStoreEntryID** <br/> |
   
Transport Anbieter-Support Objekte verfügen über Implementierungen für die folgenden Methoden:
  
||||
|:-----|:-----|:-----|
|**DoConfigPropsheet** <br/> |**CompareEntryIDs** <br/> |**CreateOneOff** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |**Getlasterroraufzurufen** <br/> |
|**IStorageFromStream** <br/> |**MakeInvalid** <br/> |**ModifyStatusRow** <br/> |
|**OpenAddressBook** <br/> |**RegisterPreprocessor** <br/> |**NewUID** <br/> |
|**Benachrichtigen** <br/> |**OpenProfileSection** <br/> |**OpenEntry** <br/> |
|**StatusRecips** <br/> |**SpoolerNotify** <br/> |**SpoolerYield** <br/> |
|**WrapStoreEntryID** <br/> |**Abonnieren** <br/> |**Unsubscribe** <br/> |
   
Nachrichtendienst-Support Objekte verfügen über Implementierungen für die folgenden Methoden:
  
|||
|:-----|:-----|
|**DoConfigPropsheet** <br/> |**Getlasterroraufzurufen** <br/> |
|**GetMemAllocRoutines** <br/> |**GetSvcConfigSupportObj** <br/> |
|**MakeInvalid** <br/> |**NewUID** <br/> |
|**OpenProfileSection** <br/> |
   
## <a name="see-also"></a>Siehe auch



[MAPI-Schnittstellen](mapi-interfaces.md)

