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
ms.openlocfilehash: c77acb5226361ce31a7f6b1694de7fe23f8dd71b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315988"
---
# <a name="entryid"></a>ENTRYID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Eintrags-ID für ein MAPI-Objekt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
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
  
> Bitmaske von Flags, die Informationen zur Beschreibung des Objekts enthalten. Nur das erste Byte der Flags, **abFlags [0]**, kann vom Anbieter festgelegt werden; die anderen drei sind reserviert. Diese Flags dürfen nicht für dauerhafte Eintragsbezeichner festgelegt werden; Sie werden nur für kurzfristige Eintrags-IDs festgelegt. Für Clients ist diese Struktur schreibgeschützt. Die folgenden Flags können in **abFlags [0]** festgelegt werden:
    
MAPI_NOTRECIP 
  
> Die Eintrags-ID kann nicht als Empfänger einer Nachricht verwendet werden.
    
MAPI_NOTRESERVED 
  
> Andere Benutzer können nicht auf die Eintrags-ID zugreifen.
    
MAPI_NOW 
  
> Die Eintrags-ID kann nicht zu anderen Zeiten verwendet werden.
    
MAPI_SHORTTERM 
  
> Die Eintrags-ID ist kurzfristig. Alle anderen Werte in diesem Byte müssen festgelegt werden, es sei denn, andere Verwendungen der Eintrags-ID sind aktiviert.
    
MAPI_THISSESSION 
  
> Die Eintrags-ID kann nicht in anderen Sitzungen verwendet werden.
    
 **ab**
  
> Gibt ein Array von Binärdaten an, die von Dienstanbietern verwendet werden. Die Clientanwendung kann dieses Array nicht verwenden.
    
## <a name="remarks"></a>Bemerkungen

Die **Eintrags** -ID-Struktur wird vom Nachrichtenspeicher und den Adressbuch Anbietern verwendet, um eindeutige Bezeichner für Ihre Objekte zu erstellen. Eintrags-IDs werden verwendet, um die folgenden Objekttypen zu identifizieren: 
  
- Nachrichtenspeicher
    
- Ordner
    
- Nachrichten
    
- Adressbuchcontainer
    
- Verteilerlisten
    
- Messaging Benutzer
    
- Statusobjekte
    
- Profilabschnitte
    
Jeder Anbieter verwendet ein Format für die **Eintrags** -Struktur, die für diesen Anbieter sinnvoll ist. 
  
Eintragsbezeichner lassen sich nicht direkt miteinander vergleichen, da ein Objekt durch zwei unterschiedliche binäre Werte dargestellt werden kann. Rufen Sie die [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) -Methode auf, um zu bestimmen, ob zwei Eintragsbezeichner dasselbe Objekt darstellen. 
  
Wenn ein Client die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode eines Objekts zum Abrufen seiner Eintrags-ID aufruft, gibt das Objekt die dauerhaftste Form der Eintrags-ID zurück. Ein Client kann überprüfen, ob eine Eintrags-ID langfristig ist, indem er überprüft, ob keines der Flags im ersten Byte des **abFlags** -Members festgelegt ist. 
  
Wenn ein Client über eine Spalte in einer Tabelle auf eine Eintrags-ID zugreift, ist dieser Eintragsbezeichner höchstwahrscheinlich kurzfristig und nicht langfristig. Mit kurzfristigen Eintrags-IDs können die entsprechenden Objekte nur in der aktuellen MAPI-Sitzung geöffnet werden. Ein Client kann überprüfen, ob eine Eintrags-ID kurzfristig ist, indem er überprüft, ob alle Flags im ersten Byte des **abFlags** -Members festgelegt sind. 
  
Einige Eintrags-IDs sind kurzfristig, haben aber langfristige Verwendung. Eine solche Eintrags-ID verfügt über eine oder mehrere der entsprechenden Flags, die im ersten Byte des **abFlags** -Elements festgelegt sind. 
  
Eine **Eintrags** -Struktur ähnelt einer [FLATENTRY](flatentry.md) -Struktur. Es gibt jedoch einige Unterschiede: 
  
- Die **** Größe der Eintrags-ID wird von einer Eintragsstruktur nicht gespeichert. eine **FLATENTRY** -Struktur. 
    
- Eine **Eintrags** -ID speichert die kennzeichendaten und den Rest des Eintrags Bezeichners separat; eine **FLATENTRY** -Struktur speichert die kennzeichendaten mit dem Rest der Eintrags-ID. 
    
- Eine **Eintrags** -Struktur wird als Parameter an die Methoden der [IMAPIProp](imapipropiunknown.md) -Schnittstelle und an die folgenden **OpenEntry** -Methoden übergeben: [IABLogon:: OpenEntry](iablogon-openentry.md), [IAddrBook::](iaddrbook-openentry.md)OpenEntry, [IMAPIContainer:: OpenEntry ](imapicontainer-openentry.md), [IMAPISession::](imapisession-openentry.md)OpenEntry, [IMAPISupport::](imapisupport-openentry.md)OpenEntry, [IMsgStore::](imsgstore-openentry.md)OpenEntry, [IMSLogon::](imslogon-openentry.md) OpenEntry
    
- Eine **Eintrags** Struktur wird verwendet, um eine Eintrags-ID auf dem Datenträger zu speichern. Eine **FLATENTRY** -Struktur wird verwendet, um eine Eintrags-ID in einer Datei zu speichern oder in einem Stream von Bytes zu übertragen. 
    
Clients sollten immer in natürlich ausgerichteten Eintrags Bezeichnern bestehen. Obwohl Anbieter willkürlich ausgerichtete Eintrags-IDs behandeln sollten, sollten Clients dieses Verhalten nicht erwarten. Fehler bei der Übergabe einer gut ausgerichteten Eintrags-ID an eine Methode können einen Ausrichtungsfehler auf RISC-Prozessoren verursachen. 
  
Der natürliche Ausrichtungs Faktor (in der Regel 8 Byte) ist der größte von der CPU unterstützte Datentyp und in der Regel derselbe Ausrichtungs Faktor, der von der systemspeicherzuweisung verwendet wird. Eine natürlich ausgerichtete Speicheradresse ermöglicht der CPU den Zugriff auf jeden Datentyp, der an dieser Adresse unterstützt wird, ohne einen Ausrichtungsfehler zu generieren. Bei RISC-CPUs muss ein Datentyp der Größe N Byte in der Regel auf einem geraden Vielfachen von N Bytes ausgerichtet werden, wobei die Adresse ein gerades Vielfaches von N ist.
  
Weitere Informationen finden Sie unter [Entry Identifiers](mapi-entry-identifiers.md). 
  
## <a name="see-also"></a>Siehe auch



[FLATENTRY](flatentry.md)
  
[IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md)
  
[Kanonische Pidtagrecordkey (-Eigenschaft](pidtagrecordkey-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

