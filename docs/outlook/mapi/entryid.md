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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415271"
---
# <a name="entryid"></a>ENTRYID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Eintragsbezeichner für ein MAPI-Objekt. 
  
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

## <a name="members"></a>Elemente

 **abFlags**
  
> Bitmaske von Flags, die Informationen bereitstellen, die das Objekt beschreiben. Nur das erste Byte der Flags, **abFlags[0]**, kann vom Anbieter festgelegt werden. die anderen drei sind reserviert. Diese Kennzeichen dürfen nicht für permanente Eintragsbezeichner festgelegt werden. sie werden nur für kurzfristige Eintragsbezeichner festgelegt. Für Clients ist diese Struktur schreibgeschützt. Die folgenden Flags können in **abFlags[0]** festgelegt werden:
    
MAPI_NOTRECIP 
  
> Der Eintragsbezeichner kann nicht als Empfänger für eine Nachricht verwendet werden.
    
MAPI_NOTRESERVED 
  
> Andere Benutzer können nicht auf die Eintrags-ID zugreifen.
    
MAPI_NOW 
  
> Der Eintragsbezeichner kann zu anderen Zeiten nicht verwendet werden.
    
MAPI_SHORTTERM 
  
> Der Eintragsbezeichner ist kurzfristig. Alle anderen Werte in diesem Byte müssen festgelegt werden, es sei denn, andere Verwendungen der Eintrags-ID sind aktiviert.
    
MAPI_THISSESSION 
  
> Der Eintragsbezeichner kann nicht für andere Sitzungen verwendet werden.
    
 **ab**
  
> Gibt ein Array von Binärdaten an, das von Dienstanbietern verwendet wird. Die Clientanwendung kann dieses Array nicht verwenden.
    
## <a name="remarks"></a>Hinweise

Die **ENTRYID-Struktur** wird von Nachrichtenspeicher- und Adressbuchanbietern verwendet, um eindeutige Bezeichner für ihre Objekte zu erstellen. Eingabebezeichner werden verwendet, um die folgenden Objekttypen zu identifizieren: 
  
- Nachrichtenspeicher
    
- Ordner
    
- Nachrichten
    
- Adressbuchcontainer
    
- Verteilerlisten
    
- Messagingbenutzer
    
- Statusobjekte
    
- Profilabschnitte
    
Jeder Anbieter verwendet ein Format für die **ENTRYID-Struktur,** das für diesen Anbieter sinnvoll ist. 
  
Eintragsbezeichner lassen sich nicht direkt miteinander vergleichen, da ein Objekt durch zwei unterschiedliche binäre Werte dargestellt werden kann. Um zu bestimmen, ob zwei Eintragsbezeichner dasselbe Objekt darstellen, rufen Sie die [IMAPISession::CompareEntryIDs-Methode](imapisession-compareentryids.md) auf. 
  
Wenn ein Client die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) eines Objekts aufruft, um den Eintragsbezeichner abzurufen, gibt das Objekt die dauerhafteste Form der Eintrags-ID zurück. Ein Client kann überprüfen, ob ein Eintragsbezeichner langfristig ist, indem er überprüft, ob keines der Kennzeichen im ersten Byte des **abFlags-Mitglieds festgelegt** ist. 
  
Wenn ein Client über eine Spalte in einer Tabelle auf einen Eintragsbezeichner zutritt, ist dieser Eintragsbezeichner höchstwahrscheinlich kurz- statt langfristig. Kurzfristige Eintragsbezeichner können nur in der aktuellen MAPI-Sitzung verwendet werden, um die entsprechenden Objekte zu öffnen. Ein Client kann überprüfen, ob ein Eintragsbezeichner kurzfristig ist, indem er überprüft, ob alle Kennzeichen im ersten Byte des **abFlags-Mitglieds festgelegt** sind. 
  
Einige Eintragsbezeichner sind kurzfristig, haben aber eine langfristige Verwendung. Für einen solchen Eintragsbezeichner wird mindestens eines der entsprechenden Flags im ersten Byte des **abFlags-Mitglieds festgelegt.** 
  
Eine **ENTRYID-Struktur** ähnelt einer [FLATENTRY-Struktur.](flatentry.md) Es gibt jedoch einige Unterschiede: 
  
- In **einer ENTRYID-Struktur** wird die Größe der Eintrags-ID nicht gespeichert. eine **FLATENTRY-Struktur.** 
    
- Eine **ENTRYID-Struktur** speichert die Kennzeichendaten und den Rest der Eintrags-ID separat. Eine **FLATENTRY-Struktur** speichert die Kennzeichendaten mit dem Rest der Eintrags-ID. 
    
- Eine **ENTRYID-Struktur** wird als Parameter an die Methoden der [IMAPIProp-Schnittstelle](imapipropiunknown.md) und an die folgenden **OpenEntry-Methoden** übergeben: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Eine **ENTRYID-Struktur** wird verwendet, um eine Eintrags-ID auf dem Datenträger zu speichern. Eine **FLATENTRY-Struktur** wird verwendet, um eine Eintrags-ID in einer Datei zu speichern oder sie in einem Bytestrom zu übergeben. 
    
Clients sollten immer natürlich ausgerichtete Eintragsbezeichner übergeben. Obwohl Anbieter willkürlich ausgerichtete Eintragsbezeichner behandeln sollten, sollten Clients dieses Verhalten nicht erwarten. Wenn eine gute ausgerichtete Eintrags-ID nicht an eine Methode übergeben wird, kann dies zu einem Ausrichtungsfehler bei RISC-Prozessoren führen. 
  
Der natürliche Ausrichtungsfaktor (in der Regel 8 Byte) ist der größte datentyp, der von der CPU unterstützt wird, und in der Regel der gleiche Ausrichtungsfaktor, der von der Systemspeicherzuweisung verwendet wird. Eine natürlich ausgerichtete Speicheradresse ermöglicht der CPU den Zugriff auf jeden datentyp, den sie an dieser Adresse unterstützt, ohne einen Ausrichtungsfehler zu generieren. Für RISC-CPUs muss ein Datentyp der Größe N Bytes in der Regel an einem geraden Vielfachen von N Bytes ausgerichtet werden, bei der Adresse ist ein gerades Vielfaches von N.
  
Weitere Informationen finden Sie unter [Entry Identifiers](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>Siehe auch



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[PidTagRecordKey (kanonische Eigenschaft)](pidtagrecordkey-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

