---
title: ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.ENTRYID
api_type:
- COM
ms.assetid: 8ebb21ca-5ad1-4dcc-97b6-2390664b5d8d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2922a242a0ac3ebbd071a85fb49ce9375a4cb22f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630943"
---
# <a name="entryid"></a>ENTRYID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält einen Eintragsbezeichner für ein MAPI-Objekt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbNewENTRYID](cbnewentryid.md), [SizeENTRYID](sizedentryid.md) <br/> |
   
```cpp
typedef struct
{
  BYTE abFlags[4];
  BYTE ab[MAPI_DIM];
} ENTRYID, FAR *LPENTRYID;

```

## <a name="members"></a>Members

 **abFlags**
  
> Bitmaske von Flags, die Informationen bereitstellen, die das Objekt beschreiben. Nur das erste Byte der Flags, **abFlags[0]**, kann vom Anbieter festgelegt werden. die anderen drei sind reserviert. Diese Flags dürfen nicht für dauerhafte Eintragsbezeichner festgelegt werden. sie werden nur für kurzfristige Eintragsbezeichner festgelegt. Für Clients ist diese Struktur schreibgeschützt. Die folgenden Flags können in **abFlags[0]** festgelegt werden:
    
MAPI_NOTRECIP 
  
> Der Eintragsbezeichner kann nicht als Empfänger einer Nachricht verwendet werden.
    
MAPI_NOTRESERVED 
  
> Andere Benutzer können nicht auf den Eintragsbezeichner zugreifen.
    
MAPI_NOW 
  
> Der Eintragsbezeichner kann nicht zu anderen Zeiten verwendet werden.
    
MAPI_SHORTTERM 
  
> Der Eintragsbezeichner ist kurzfristig. Alle anderen Werte in diesem Byte müssen festgelegt werden, es sei denn, andere Verwendungsmöglichkeiten des Eintragsbezeichners sind aktiviert.
    
MAPI_THISSESSION 
  
> Der Eintragsbezeichner kann nicht in anderen Sitzungen verwendet werden.
    
 **ab**
  
> Gibt ein Array binärer Daten an, das von Dienstanbietern verwendet wird. Die Clientanwendung kann dieses Array nicht verwenden.
    
## <a name="remarks"></a>Bemerkungen

Die **ENTRYID-Struktur** wird von Nachrichtenspeicher- und Adressbuchanbietern verwendet, um eindeutige Bezeichner für ihre Objekte zu erstellen. Eintragsbezeichner werden verwendet, um die folgenden Objekttypen zu identifizieren: 
  
- Nachrichtenspeicher
    
- Ordner
    
- Nachrichten
    
- Adressbuchcontainer
    
- Verteilerlisten
    
- Messaging-Benutzer
    
- Statusobjekte
    
- Profilabschnitte
    
Jeder Anbieter verwendet ein Format für die **ENTRYID-Struktur,** das für diesen Anbieter sinnvoll ist. 
  
Eintragsbezeichner lassen sich nicht direkt miteinander vergleichen, da ein Objekt durch zwei unterschiedliche binäre Werte dargestellt werden kann. Rufen Sie die [IMAPISession::CompareEntryIDs-Methode](imapisession-compareentryids.md) auf, um zu bestimmen, ob zwei Eintragsbezeichner dasselbe Objekt darstellen. 
  
Wenn ein Client die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) eines Objekts aufruft, um den Eintragsbezeichner abzurufen, gibt das Objekt die dauerhafteste Form des Eintragsbezeichners zurück. Ein Client kann überprüfen, ob ein Eintragsbezeichner langfristig ist, indem überprüft wird, ob keines der Flags im ersten Byte des **abFlags-Elements** festgelegt ist. 
  
Wenn ein Client über eine Spalte in einer Tabelle auf einen Eintragsbezeichner zugreift, ist dieser Eintragsbezeichner höchstwahrscheinlich kurzfristig statt langfristig. Bezeichner für kurzfristige Einträge können verwendet werden, um ihre entsprechenden Objekte nur in der aktuellen MAPI-Sitzung zu öffnen. Ein Client kann überprüfen, ob ein Eintragsbezeichner kurzfristig ist, indem er überprüft, ob alle Flags im ersten Byte des **abFlags-Mitglieds** festgelegt sind. 
  
Einige Eintragsbezeichner sind kurzfristig, werden aber langfristig verwendet. Für einen solchen Eintragsbezeichner wird mindestens ein entsprechendes Flag im ersten Byte des **abFlags-Elements** festgelegt. 
  
Eine **ENTRYID-Struktur** ähnelt einer [FLATENTRY-Struktur.](flatentry.md) Es gibt jedoch einige Unterschiede: 
  
- Eine **ENTRYID-Struktur** speichert nicht die Größe des Eintragsbezeichners. Eine **FLATENTRY-Struktur** hat dies. 
    
- In einer **ENTRYID-Struktur** werden die Kennzeichendaten und der Rest des Eintragsbezeichners separat gespeichert. Eine **FLATENTRY-Struktur** speichert die Kennzeichendaten mit dem restlichen Eintragsbezeichner. 
    
- Eine **ENTRYID-Struktur** wird als Parameter an die Methoden der [IMAPIProp-Schnittstelle](imapipropiunknown.md) und an die folgenden **OpenEntry-Methoden** übergeben: [IABLogon::OpenEntry](iablogon-openentry.md), [IAddrBook::OpenEntry](iaddrbook-openentry.md), [IMAPIContainer::OpenEntry](imapicontainer-openentry.md), [IMAPISession::OpenEntry](imapisession-openentry.md), [IMAPISupport::OpenEntry](imapisupport-openentry.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), [IMSLogon::OpenEntry](imslogon-openentry.md)
    
- Eine **ENTRYID-Struktur** wird verwendet, um einen Eintragsbezeichner auf dem Datenträger zu speichern. Eine **FLATENTRY-Struktur** wird verwendet, um einen Eintragsbezeichner in einer Datei zu speichern oder in einem Bytestream zu übergeben. 
    
Clients sollten immer natürlich ausgerichtete Eintragsbezeichner übergeben. Obwohl Anbieter willkürlich ausgerichtete Eintragsbezeichner behandeln sollten, sollten Clients dieses Verhalten nicht erwarten. Wenn eine gut ausgerichtete Eintrags-ID nicht an eine Methode übergeben wird, kann dies zu einem Ausrichtungsfehler auf RISC-Prozessoren führen. 
  
Der natürliche Ausrichtungsfaktor (in der Regel 8 Byte) ist der größte datentyp, der von der CPU unterstützt wird, und in der Regel derselbe Ausrichtungsfaktor, der von der Systemspeicherzuweisung verwendet wird. Eine natürlich ausgerichtete Speicheradresse ermöglicht der CPU den Zugriff auf jeden Datentyp, den sie an dieser Adresse unterstützt, ohne einen Ausrichtungsfehler zu generieren. Bei RISC-CPUs muss ein Datentyp der Größe N Bytes in der Regel an einem geraden Vielfachen von N Bytes ausgerichtet werden, wobei die Adresse ein gerades Vielfaches von N ist.
  
Weitere Informationen finden Sie unter [Eintragsbezeichner.](mapi-entry-identifiers.md) 
  
## <a name="see-also"></a>Siehe auch



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Kanonische PidTagRecordKey-Eigenschaft](pidtagrecordkey-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

