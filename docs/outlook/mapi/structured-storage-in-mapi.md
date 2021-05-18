---
title: Strukturierte Storage in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f58fa70e98841db5507323a63737f1df6c1b7a6d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411750"
---
# <a name="structured-storage-in-mapi"></a>Strukturierte Storage in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Strukturierter Speicher bezieht sich auf die hierarchische Organisation des Speichers, die mit COM eingeführt wurde. In einer strukturierten Speicherumgebung ist der Speicher in zwei oder drei Arten von Objekten organisiert: 
  
- Stream-Objekte
    
- Sperren von Byteobjekten
    
- Storage-Objekte
    
Stream- und Sperrbytes sind Objekte auf niedrigerer Ebene, die direkt auf die Daten zugreifen. Stream-Objekte implementieren die **IStream-Schnittstelle,** die Methoden zum Lesen, Schreiben, Positionieren und Kopieren von Bytes von Daten definiert. Lock Bytes-Objekte implementieren eine weitere COM-Schnittstelle, **ILockBytes**, um auf Daten mit einem Bytearray zu zugreifen. Bytearrays werden in der Regel verwendet, um benutzerdefinierten Zugriff auf den zugrunde liegenden Speicher zu ermöglichen.
  
Storage Objekte werden über dem Stream oder dem Sperren von Byteobjekten überschichtet. sie können eines oder mehrere dieser Objekte sowie andere Speicherobjekte enthalten. Storage-Objekte implementieren die **IStorage-Schnittstelle,** die Methoden zum Erstellen, Zugreifen und Verwalten geschachtelter Objekte definiert. 
  
Da **IStream,** **ILockBytes** und **IStorage** KEINE MAPI-Schnittstellen, sondern COM-Schnittstellen sind, geben ihre Methoden COM-Fehlerwerte anstelle von MAPI-Werten zurück. Clients und Dienstanbieter, die Methoden in diesen Schnittstellen aufrufen, müssen die API-Funktion **MapStorageSCode** verwenden, um diese Werte in MAPI-Fehlerwerte zu übersetzen. Weitere Informationen finden Sie unter [MapStorageSCode](mapstoragescode.md).
  
Clients und Dienstanbieter verwenden strukturierten Speicher für die Arbeit mit Eigenschaften, die zu groß sind, um sie mit den **IMAPIProp-Methoden** zu verwalten, in der Regel große Zeichenfolgen- und binäre Eigenschaften. Eine der gängigen Methoden, auf die Clients oder Dienstanbieter zugreifen, besteht in der Angabe von **IStream** oder **IStorage** als Schnittstellenbezeichner in einem Aufruf der [IMAPIProp::OpenProperty-Methode.](imapiprop-openproperty.md) Clients rufen z. B. **OpenProperty** mit **PR_ATTACH_DATA_BIN** als Eigenschaftstag und IID_IStream als Schnittstellen-ID auf, um auf eine binäre Anlage in einer Nachricht zu zugreifen. 
  
Clients und Dienstanbieter können eigene Stream- und Speicherobjekte implementieren oder API-Funktionen aufrufen, um auf von MAPI oder COM bereitgestellte Implementierungen zu zugreifen. Da die bereitgestellten Implementierungen den meisten Zwecken dienen, müssen Clients und Dienstanbieter selten eigene Erstellen. 
  
Wenn ein Client **OpenProperty für** ein MAPI-Objekt aufruft, um über ein Speicherobjekt auf eine seiner Eigenschaften zu zugreifen, öffnet der Dienstanbieter das Speicherobjekt in der Regel im direkten Modus. Dies ist jedoch ein typisches und nicht erforderliches Verhalten. Clients sollten davon ausgehen, dass alle von Dienstanbietern geöffneten oder erstellten Speicherobjekte transaktiviert werden und einen Aufruf von **IStorage::Commit erfordern.** Sie sollten auch bedenken, dass Änderungen an Speicherobjekten erst dauerhaft vorgenommen werden, wenn **sie IMAPIProp::SaveChanges** nach dem letzten **Commit** zum Speichern des MAPI-Objekts aufrufen. Weitere Informationen finden Sie unter [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
  
MAPI und COM bieten verschiedene API-Funktionen zum Definieren oder Zugreifen auf Speicher- und Streamobjekte. Die häufig verwendeten Funktionen werden in der folgenden Tabelle beschrieben.
  
**Funktionen für den Zugriff Storage und Stream-Objekte**

|**Funktion**|**Beschreibung**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Erstellt ein Speicherobjekt für den Zugriff auf ein Stream- oder Sperrbyteobjekt.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Erstellt ein Nachrichtenobjekt für den Zugriff auf ein Speicherobjekt.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Erstellt ein Streamobjekt für den Zugriff auf eine Datei.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Erstellt ein Streamobjekt, das die komprimierte oder nicht komprimierte Version eines Datenstroms mit dem Rich-Text einer Nachricht enthält.  <br/> |
   
 **So rufen Sie die Namen der Datenströme in einem bestimmten Unterordner ab**
  
1. Rufen Sie die **IStorage::EnumElements-Methode** des Unterordners auf, um eine **IEnumSTATSTG-Schnittstelle zu** erhalten. 
    
2. Rufen **Sie IEnumSTATSTG::Next** mit möglichst vielen **STATSTG-Strukturen** gleichzeitig auf. Wenn Sie gleichzeitig nach 100 fragen, gibt **Next** in der Regel S_FALSE zurück, bei dem der Inhalt von  _pceltFetched_ auf die Tatsächlich abgerufene Nummer festgelegt ist. 
    
3. Suchen Sie nach **den STATSTG-Strukturen,** die mit STGTY_STREAM. 
    
4. Geben Sie den  _pwcsName-Parameter_ frei. 
    
 **So erstellen Sie ein Speicherobjekt für den Zugriff auf ein vorhandenes Stream- oder Sperrbyteobjekt**
  
- Clients rufen [HrIStorageFromStream auf.](hristoragefromstream.md) 
    
 **So erstellen Sie ein Nachrichtenobjekt für den Zugriff auf ein vorhandenes Speicherobjekt**
  
- Dienstanbieter und Clients rufen [OpenIMsgOnIStg auf.](openimsgonistg.md) Das erstellte Nachrichtenobjekt unterscheidet sich von den Nachrichtenobjekten, die normalerweise von Nachrichtenspeicheranbietern erstellt werden, da es nicht alle [IMessage : IMAPIProp-Schnittstellenmethoden](imessageimapiprop.md) unterstützt, z. B. **IMessage::SubmitMessage**. Ein optionaler Eingabeparameter für **OpenIMsgOnIStg** ist eine Rückruffunktion, die dem [MSGCALLRELEASE-Prototyp entspricht.](msgcallrelease.md) Diese Funktion wird vom neuen Message-Objekt aufgerufen, wenn die Referenzanzahl der Nachricht null erreicht. Das Implementieren einer **MSGCALLRELEASE-Funktion** kann für die endgültige Verarbeitung nützlich sein, bevor die neue Nachricht vollständig entfernt wird. 
    
[OpenStreamOnFile](openstreamonfile.md) wird häufig zum Speichern von Dateianlagen verwendet, da es einen Datenstrom erstellt, der aus einer Datei liest und in eine Datei schreibt. **OpenProperty** mit **PR_ATTACH_DATA_BIN** als Eigenschaftstag erstellt einen Datenstrom zum Speichern binärer Anlagendaten. 
  
 **So komprimieren oder entkomprimieren Sie einen Datenstrom mit Nachrichtentext im Rich-Text-Format**
  
- Clients rufen [WrapCompressedRTFStream auf.](wrapcompressedrtfstream.md) **WrapCompressedRTFStream** erstellt einen Datenstrom, der den RTF-Stream umschließt. Der Wrapperstream implementiert nicht alle **IStream-Methoden.** Die folgenden Methoden werden ausgeschlossen: **Seek**, **SetSize**, **Revert**, **LockRegion**, **UnlockRegion**, **Stat** und **Clone**. Dies liegt daran, dass die von **WrapCompressedRTFStream** erstellten Streamobjekte **weder SetSize** noch **Stat** unterstützen. Es gibt keine einfache Möglichkeit, ihre Größe zu erweitern oder abzurufen. Die beste Strategie besteht in der Auswahl einer angemessenen Puffergröße und dem Lesen oder Schreiben in einer Schleife.
    
> [!NOTE]
> COM verfügt über eine Speicherobjektimplementierung basierend auf einem Bytearray, das ein **IEnumSTATSTG-Objekt** aus der **problematischen EnumElements-Methode** zurückgibt. Insbesondere die **QueryInterface-Methode** funktioniert nicht ordnungsgemäß. Dienstanbieter, die ihre eigenen Speicherobjekte mithilfe der COM-Implementierung implementieren, sollten einen dünnen Wrapper für das **IEnumSTATSTG-Objekt** erstellen, das Aufrufe an die zugrunde liegenden **IEnumSTATSTG-Methoden** weiter gibt, aber eigene **AddRef-,** **Release-,** **QueryInterface-** und **Clone-Methoden** implementiert. 
  

