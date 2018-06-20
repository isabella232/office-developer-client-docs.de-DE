---
title: Optionale Features für Adressbuchanbietern implementierte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ffdd1203316b2c80aba34c980745a0330ec19888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793317"
---
# <a name="optional-features-for-address-book-providers"></a>Optionale Features für Adressbuchanbietern implementierte

  
  
**Betrifft**: Outlook 
  
Es gibt zahlreiche optionale Funktionen für adressbuchanbietern implementierte. Einige der häufiger implementierten Features zählen:
  
- Durch Zulassen der Einträge aus den Containern, einen anderen Anbieter Container hinzugefügt werden soll fungiert als fremden Anbieter.
    
- Als Hostanbieter fungiert, indem Sie Einträge aus einem anderen Anbieter eines Ihre Container.
    
- Erweiterte Suche.
    
- Präfix Bildlauf durch den Inhalt Tabellen.
    
- Unterstützung für Verteilerlisten.
    
- Unterstützung für die Benachrichtigung.
    
In der folgenden Tabelle werden kurz dieser optionalen Features und deren Implementierung beschrieben:
  
|**Funktion**|**Gewusst wie: Implementieren**|
|:-----|:-----|
|Bereitstellen von Vorlagen zum Erstellen von Einträgen für Nachricht Empfängerlisten  <br/> |Implementieren Sie die [GetOneOffTable](iablogon-getoneofftable.md) -Methode. Weitere Informationen finden Sie unter [Einmaligen](one-off-tables.md) und [Einmaligen Tabellen implementieren](implementing-one-off-tables.md).  <br/> |
|Gruppe von Empfängern in einer benannten Einheit  <br/> |Unterstützung die Eigenschaften von Verteilerlisten durch die Implementierung der [IDistList: IMAPIContainer](idistlistimapicontainer.md) Schnittstelle.  <br/> |
|Fungieren Sie als einen fremden Adressbuchanbieter durch Zulassen der Einträge, einen Container in einen anderen Anbieter hinzugefügt werden soll  <br/> | Unterstützung für Bindung Code auf Daten in der Hostanbieter nach:  <br/>  Die **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md))-Eigenschaft unterstützt auf Benutzer und Verteilerlisten messaging. Weitere Informationen finden Sie unter [Address Book-IDs](address-book-identifiers.md).  <br/>  Implementieren der [OpenTemplateID](iablogon-opentemplateid.md) -Methode. Weitere Informationen finden Sie unter [als einen fremden Adressbuchanbieter fungiert](acting-as-a-foreign-address-book-provider.md).  <br/> |
|Als ein Host-Adressbuchanbieter fungiert, indem Sie Einträge aus einem anderen Anbieter einfügen  <br/> |Binden von Daten Code von einem fremden Anbieter mithilfe Aufrufen der [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) -Methode unterstützt. Weitere Informationen finden Sie unter [als ein Host-Adressbuchanbieter fungiert](acting-as-a-host-address-book-provider.md).  <br/> |
|Ausführen eines Bildlaufs Präfix  <br/> |Unterstützung von Einschränkungen Container Inhalt Tabellen. Weitere Informationen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).  <br/> |
|Erweiterte Suche in einem container  <br/> |Unterstützen Sie die **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md))-Eigenschaft auf Container. Weitere Informationen finden Sie unter [Implementieren erweiterte Suche](implementing-advanced-searching.md).  <br/> |
|Benachrichtigung bei  <br/> |Implementieren Sie die Methoden [IABLogon::Advise](iablogon-advise.md) und [IABLogon::Unadvise](iablogon-unadvise.md) . Weitere Informationen finden Sie unter [Benachrichtigung in MAPI](event-notification-in-mapi.md) und [Ereignisbenachrichtigung unterstützen](supporting-event-notification.md).  <br/> |
   
Benachrichtigung wird die **IABLogon::Advise** -Methode von MAPI aufgerufen, wenn ein Client **IAddrBook::Advise** für Benachrichtigungen auf jedem dieser den Containern registriert aufruft messaging Benutzer oder Verteilerlisten. Da Unterstützung ereignisbenachrichtigung optional ist, können Sie MAPI_E_NO_SUPPORT von diesen Methoden zurückgeben. MAPI jedoch, wird empfohlen, dass Sie mindestens auf Ihren Inhalt Tabellen unterstützen und empfiehlt eine unterstützen alle Arten von Objekt Benachrichtigung mit Ausnahme von _FnevSearchComplete_ und das Ereignis _FnevCriticalError_ Wert hinzufügen. 
  

