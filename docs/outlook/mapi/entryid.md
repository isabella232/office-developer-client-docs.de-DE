---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1b55703c9ad12e3645e6e9cb3dcfcbdf21b90d25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791631"
---
# <a name="entryid"></a>ENTRYID

  
  
**Betrifft**: Outlook 
  
Enthält einen Eintrag Bezeichner für ein MAPI-Objekt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbNewENTRYID](cbnewentryid.md), [SizedENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>Members

 **abFlags**
  
> Bitmaske aus Flags, die Informationen enthalten, die das Objekt beschreibt. Vom Anbieter kann nur auf das erste Byte des die Kennzeichen, **AbFlags [0]**, festgelegt werden. die anderen drei sind vorbehalten. Diese Flags müssen für permanente-Eintragsbezeichner nicht festgelegt werden. Sie sind nur für kurzfristige-Eintragsbezeichner festgelegt. Clients ist diese Struktur schreibgeschützt. Die folgenden Kennzeichen können in **AbFlags [0]** festgelegt werden:
    
MAPI_NOTRECIP 
  
> Die Eintrags-ID kann nicht als Empfänger einer Nachricht verwendet werden.
    
MAPI_NOTRESERVED 
  
> Andere Benutzer können nicht die Eintrags-ID zugreifen.
    
MAPI_NOW 
  
> Die Eintrags-ID kann nicht in anderen Fällen verwendet werden.
    
MAPI_SHORTTERM 
  
> Die Eintrags-ID ist kurzfristige. Alle anderen Werte in Byte müssen festgelegt werden, es sei denn, weitere Verwendungsmöglichkeiten des Bezeichners Eintrag aktiviert sind.
    
MAPI_THISSESSION 
  
> Die Eintrags-ID kann nicht auf andere-Sitzungen verwendet werden.
    
 **ab**
  
> Gibt ein Array von binären Daten, die vom Dienstanbieter verwendet werden. Die Client-Anwendung kann nicht in Array verwenden.
    
## <a name="remarks"></a>Hinweise

Die **ENTRYID** -Struktur wird von der Nachricht speichern und Beheben von adressbuchanbietern implementierte zum Erstellen von eindeutiger Bezeichnern für Objekte. Eintragsbezeichner werden verwendet, um die folgenden Typen von Objekten zu identifizieren: 
  
- Nachrichtenspeicher
    
- Ordner
    
- Nachrichten
    
- Address Book Container
    
- Verteilerlisten
    
- Messaging-Benutzer
    
- Status-Objekte
    
- Profil Abschnitte
    
Jeder Provider verwendet ein Format für die **Eintrags-ID** -Struktur, die für diesen Anbieter sinnvoll sind. 
  
Eintragsbezeichner lassen sich nicht direkt miteinander vergleichen, da ein Objekt durch zwei unterschiedliche binäre Werte dargestellt werden kann. Um zu bestimmen, ob zwei Eintragsbezeichner dasselbe Objekt darstellen, rufen Sie die [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) -Methode. 
  
Wenn ein Client ein Objekt [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode, um die Eintrags-ID abrufen aufruft, gibt das Objekt am häufigsten permanente Form eines Eintrags-ID zurück. Ein Client überprüfen, ob eine Eintrags-ID langfristige ist, indem Sie überprüfen, dass keines der Flags im ersten Byte des Elements **AbFlags** festgelegt sind. 
  
Wenn ein Client greift auf eine Eintrags-ID über eine Spalte in einer Tabelle, die dieses Eintrags-ID anstelle von langfristige kurzfristige ist wahrscheinlich. Kurzfristige-Eintragsbezeichner können verwendet werden, um die entsprechenden Objekte nur in der aktuellen MAPI-Sitzung zu öffnen. Ein Client überprüfen, ob eine Eintrags-ID kurzfristige ist, indem Sie überprüfen, dass alle Kennzeichen im ersten Byte des Elements **AbFlags** festgelegt sind. 
  
Einige Eintragsbezeichner sind kurzfristig, aber langfristige verwenden. Solche Eintrags-ID wird mindestens eines der entsprechenden Flags, die in dem ersten Byte des **AbFlags** Mitglied festgelegt haben. 
  
Eine Struktur **ENTRYID** ähnelt eine [FLATENTRY](flatentry.md) Struktur. Es gibt jedoch einige Unterschiede: 
  
- Eine **ENTRYID** -Struktur wird die Größe des Eintrags-ID nicht gespeichert; Es wird eine **FLATENTRY** -Struktur. 
    
- Eine Struktur **ENTRYID** speichert die Flag-Daten und den Rest des Bezeichners Eintrag separat; eine Struktur **FLATENTRY** speichert die Kennzeichnungsdaten mit dem Rest der Eintrags-ID an. 
    
- Eine **ENTRYID** -Struktur wird als Parameter übergeben, an die Methoden der Schnittstelle [IMAPIProp](imapipropiunknown.md) und auf die folgenden Methoden **OpenEntry** : [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry ](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Eine **ENTRYID** -Struktur wird verwendet, um die Eintrags-ID auf dem Datenträger speichern. Eine Struktur **FLATENTRY** wird verwendet, um eine Eintrags-ID in einer Datei speichern, oder geben Sie ihn in einen Datenstrom von Bytes. 
    
Clients sollte immer natürlich ausgerichtet-Eintragsbezeichner übergeben. Obwohl Anbieter willkürlich ausgerichtete-Eintragsbezeichner behandelt werden sollen, sollten Clients dieses Verhalten nicht erwarten. Eine gute ausgerichtete Eintrags-ID an eine Methode übergeben können Ausrichtungsfehler durch eine auf RISC-Prozessoren führen. 
  
Der natürlichen Ausrichtung Faktor, in der Regel 8 Byte ist der größte Datentyp, der von der CPU unterstützt und in der Regel den gleichen Ausrichtung Faktor durch das System Arbeitsspeicher Zuweisung verwendet. Eine Adresse natürlich ausgerichteten Speicher ermöglicht die CPU auf einen beliebigen Datentyp zugreifen, die sie an dieser Adresse unterstützt ohne Ausrichtungsfehler durch eine generieren. Für RISC CPUs muss ein Datentyp der Größe N Bytes in der Regel auf kein Vielfaches von N Bytes, mit der Adresse wird kein Vielfaches von n ausgerichtet werden
  
Weitere Informationen finden Sie unter [Eintragsbezeichner](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>Siehe auch



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Kanonische PidTagRecordKey-Eigenschaft](pidtagrecordkey-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

