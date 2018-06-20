---
title: Strukturierte Speicher in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 462ee84d5e9acd26f80bae6516179f21651749be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795664"
---
# <a name="structured-storage-in-mapi"></a>Strukturierte Speicher in MAPI

  
  
**Betrifft**: Outlook 
  
Strukturierter Speicher bezieht sich auf die hierarchische Organisation der Speicher mit COM eingeführt In einer Umgebung mit strukturierten Speicher ist Speicher in zwei oder drei Typen von Objekten unterteilt: 
  
- Stream-Objekten
    
- Sperren von Objekten bytes
    
- Speicherobjekte
    
Stream und Sperre Bytes sind Low-Level-Objekte, die direkt auf die Daten zugreifen. Stream-Objekten implementieren die **IStream** -Schnittstelle die Methoden zum Lesen, schreiben, Positionierung und kopieren Bytes Daten definiert. Sperren von Bytes Objekten Implementieren einer anderen COM-Schnittstelle, **ILockBytes**Zugriff auf Daten mit einem Bytearray. Byte-Arrays werden normalerweise verwendet, um angepasste Zugriff auf die zugrunde liegende Speicher bereitzustellen.
  
Speicherobjekte werden auf den Datenstrom oder Sperrtyp Byte-Objekten layered; Sie können eine oder mehrere dieser Objekte sowie andere Speicherobjekte enthalten. Speicherobjekte implementieren die **IStorage** -Schnittstelle die Methoden zum Erstellen, den Zugriff auf und warten geschachtelte Objekte definiert. 
  
Da **IStream** **ILockBytes**und **IStorage** COM-Schnittstellen anstelle von MAPI-Schnittstellen sind, geben Sie ihre Methoden com-Fehler statt MAPI-Werten zurück. Clients und Aufrufen von Methoden in diese Schnittstellen-Dienstanbieter müssen die API-Funktion **MapStorageSCode** verwenden, um diese Werte in MAPI-Fehlerwerte übersetzt. Weitere Informationen finden Sie unter [MapStorageSCode](mapstoragescode.md).
  
Clients und -Dienstanbieter verwenden strukturierten Speicher für das Arbeiten mit Eigenschaften, die zu groß, um mit den **IMAPIProp** Methoden in der Regel großen Zeichenfolge und binäre Eigenschaften beibehalten werden. Eine allgemeine Möglichkeit, dass Clients oder Dienstanbieter darauf zugreifen wird **IStream** oder **IStorage** als Schnittstellenbezeichner in einem Aufruf der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode. Clients rufen beispielsweise **OpenProperty** mit **PR_ATTACH_DATA_BIN** als Eigenschafts-Tag und IID_IStream als Schnittstellenbezeichner auf eine binäre Anlage in einer Nachricht zugreifen. 
  
Clients und Dienstanbieter implementieren ihrer eigenen Objekte Stream und Speicher oder rufen Sie API-Funktionen für Access Implementierungen von MAPI oder com bereitgestellt wird Da die angegebenen Implementierungen in den meisten Fällen dienen, müssen Clients und -Dienstanbieter selten eigene erstellen. 
  
Wenn ein Client-Anrufe **OpenProperty** in einem MAPI-Objekt an eine seiner Eigenschaften ein Speicherobjekt zugreifen, wird der Dienstanbieter in der Regel das Speicherobjekt in direkten Modus geöffnet. Dies ist jedoch statt erforderlichen Verhaltens typisch. Clients sollten wird davon ausgegangen, dass alle Speicherobjekte von Dienstanbietern erstellt oder geöffnet wurden durchgeführt werden und einen Anruf an **IStorage::Commit**erfordern. Sie sollten auch bedenken, dass Änderungen an Speicherobjekte nicht permanent gemacht werden, bis sie **IMAPIProp::SaveChanges** rufen Sie nach der letzten **Commit** in das MAPI-Objekt zu speichern. Weitere Informationen finden Sie unter [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
  
MAPI- und COM-bieten verschiedene API-Funktionen für definieren oder den Zugriff auf Speicher und Stream-Objekten. In der folgenden Tabelle werden die häufig verwendeten Funktionen beschrieben.
  
**Funktionen für den Zugriff auf Speicher- und Stream-Objekten**

|**Funktion**|**Beschreibung**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Erstellt ein Speicherobjekt Zugriff auf einen Datenstrom oder Sperrtyp Byte-Objekt.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Erstellt ein Message-Objekt um ein Speicherobjekt zuzugreifen.  <br/> |
|[OpenStreamOnFile nicht ausgeführt werden](openstreamonfile.md) <br/> |Erstellt ein Stream-Objekt, um eine Datei zuzugreifen.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Erstellt ein Stream-Objekt, das die komprimierte oder nicht komprimierte Version eines Stream-Objekts aufbewahren von rich-Text einer Nachricht enthält.  <br/> |
   
 **Um die Namen der Streams in einem bestimmten Substorage abzurufen**
  
1. Rufen Sie die Substorage **IStorage::EnumElements** -Methode, um eine **IEnumSTATSTG** Schnittstelle abzurufen. 
    
2. Rufen Sie **IEnumSTATSTG::Next** mit beliebig viele **STATSTG** -Strukturen zu einem Zeitpunkt wie möglich. Wenn Sie jeweils 100 bitten, zurückgegebenen **nächste** in der Regel S_FALSE mit dem Inhalt des _PceltFetched_ legen die Nummer, die tatsächlich abgerufen wurden. 
    
3. Überprüfen Sie die **STATSTG** -Strukturen, die mit STGTY_STREAM gekennzeichnet wurden. 
    
4. Freigeben Sie den Parameter _PwcsName_ . 
    
 **Zum Erstellen eines Speicherobjekts, um ein vorhandenes Stream oder Sperren-Byte-Objekt zuzugreifen**
  
- Clients aufrufen [HrIStorageFromStream](hristoragefromstream.md). 
    
 **Zum Erstellen eines Message-Objekts, um ein vorhandenes Speicherobjekt zugreifen**
  
- Rufen [OpenIMsgOnIStg](openimsgonistg.md)-Dienstanbieter und Clients. Message-Objekts, das erstellt wird unterscheidet sich von der Message-Objekte in der Regel Zeichenfolgeneigenschaften Nachricht erstellt, dass sie alle nicht unterstützt der [IMessage: IMAPIProp](imessageimapiprop.md) Schnittstellenmethoden wie **IMessage::SubmitMessage**. Ein optionaler Eingabeparameter für **OpenIMsgOnIStg** ist eine Rückruffunktion, die den [MSGCALLRELEASE](msgcallrelease.md) Prototyp entspricht. Diese Funktion wird durch die neue Nachrichtenobjekt aufgerufen, wenn die Nachricht Referenzzähler 0 (null) erreicht. Implementieren eine **MSGCALLRELEASE** -Funktion kann hilfreich sein für die Ausführung der letzten Verarbeitung, bevor die neue Nachricht vollständig entfernt wird. 
    
[OpenStreamOnFile nicht ausgeführt werden](openstreamonfile.md) wird häufig zum Speichern von Dateianlagen, da es einen Datenstrom erstellt, der liest aus und schreibt in eine Datei, verwendet. **OpenProperty** mit **PR_ATTACH_DATA_BIN** als das Eigenschafts-Tag erstellt einen Stream für die binären Anlagedaten zu speichern. 
  
 **Zum Komprimieren und Dekomprimieren einen Stream mit Nachrichtentext in der Rich-Text-Format**
  
- Clients aufrufen [WrapCompressedRTFStream](wrapcompressedrtfstream.md). **WrapCompressedRTFStream** erstellt einen Stream, der den RTF-Stream umbrochen wird. Der Wrapper-Stream implementiert keine alle **IStream** Methoden. die folgenden Methoden werden ausgeschlossen: **Seek**, **SetSize**, **Wiederherstellen**, **LockRegion**, **UnlockRegion**, **Stat**und **Wenn Sie den Klon**. Dies ist, da die Streamobjekte, die von **WrapCompressedRTFStream** erstellt keine **SetSize** oder **Stat**unterstützen, ist es keine einfache Möglichkeit zum Erweitern oder ihre Größe abzurufen. Die beste Strategie ist, wählen Sie eine angemessene Puffergröße sowie das Lesen oder Schreiben in einer Schleife.
    
> [!NOTE]
> COM basiert auf einer Speicher-objektimplementierung basierend auf Bytearray zurück, die ein **IEnumSTATSTG** -Objekt aus der **EnumElements** -Methode zurückgibt, die problematisch ist. Insbesondere, das die **QueryInterface** -Methode funktioniert nicht ordnungsgemäß. Dienstanbieter, die ihre eigenen Speicherobjekte mithilfe der COM-Implementierung implementieren sollten erstellen einen thin Wrapper für die **IEnumSTATSTG** -Objekt, leitet Anrufe an die zugrunde liegenden **IEnumSTATSTG** -Methoden, aber implementiert, eine eigene **AddRef **, **Version**, **QueryInterface**und **Clone** -Methoden. 
  

