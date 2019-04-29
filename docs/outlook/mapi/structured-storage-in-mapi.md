---
title: Strukturierter Speicher in MAPI
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
# <a name="structured-storage-in-mapi"></a>Strukturierter Speicher in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Structured Storage bezieht sich auf die hierarchische Organisation von Speicher, die mit COM eingeführt wird. In einer strukturierten Speicherumgebung ist der Speicher in zwei oder drei Objekttypen gegliedert: 
  
- Stream-Objekte
    
- Sperren von Bytes-Objekten
    
- Speicherobjekte
    
Stream-und Lock-Bytes sind Objekte auf niedrigerer Ebene, die direkt auf die Daten zugreifen. Stream-Objekte implementieren die **IStream** -Schnittstelle, die Methoden zum Lesen, schreiben, positionieren und Kopieren von Datenbytes definiert. Sperren von Bytes-Objekten implementieren eine andere COM-Schnittstelle, **ILockBytes**, für den Zugriff auf Daten mit einem Bytearray. Byte Arrays werden in der Regel verwendet, um benutzerdefinierten Zugriff auf zugrunde liegenden Speicher bereitzustellen.
  
Speicherobjekte werden über die Stream-oder Lock Bytes-Objekte überlagert; Sie können eines oder mehrere dieser Objekte sowie andere Speicherobjekte enthalten. Speicherobjekte implementieren die **IStorage** -Schnittstelle, die Methoden zum Erstellen, zugreifen und warten verschachtelter Objekte definiert. 
  
Da **IStream**-, **ILockBytes**-und **IStorage** -com-Schnittstellen statt MAPI-Schnittstellen sind, geben ihre Methoden com-Fehlerwerte anstelle von MAPI-Werten zurück. Clients und Dienstanbieter, die Methoden in diesen Schnittstellen aufrufen, müssen die API-Funktion **MapStorageSCode** verwenden, um diese Werte in MAPI-Fehlerwerte zu übersetzen. Weitere Informationen finden Sie unter [MapStorageSCode](mapstoragescode.md).
  
Clients und Dienstanbieter verwenden strukturierten Speicher zum Arbeiten mit Eigenschaften, die zu umfangreich sind, um mit den **IMAPIProp** -Methoden, in der Regel eine hohe Zeichenfolge und binäre Eigenschaften zu verwalten. Eine der gängigen Methoden für den Zugriff durch Clients oder Dienstanbieter ist das Angeben von **IStream** oder **IStorage** als Schnittstellenbezeichner in einem Aufruf der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode. Beispielsweise rufen Clients **OpenProperty** mit **PR_ATTACH_DATA_BIN** als Property-Tag und IID_IStream als Schnittstellenbezeichner auf, um auf eine binäre Anlage in einer Nachricht zuzugreifen. 
  
Clients und Dienstanbieter können eigene Stream-und Speicherobjekte implementieren oder API-Funktionen aufrufen, um auf von MAPI oder COM bereitgestellte Implementierungen zuzugreifen. Da die bereitgestellten Implementierungen die meisten Zwecke erfüllen, müssen Clients und Dienstanbieter selten eigene erstellen. 
  
Wenn ein Client **OpenProperty** für ein MAPI-Objekt aufruft, um über ein Speicherobjekt auf eine seiner Eigenschaften zuzugreifen, wird das Speicherobjekt in der Regel vom Dienstanbieter im Direktmodus geöffnet. Dies ist jedoch eher ein typisches als das erforderliche Verhalten. Clients sollten davon ausgehen, dass alle von Dienstanbietern geöffneten oder erstellten Speicherobjekte abgewickelt werden und einen Aufruf von **IStorage:: Commit**erfordern. Außerdem sollten Sie Bedenken, dass Änderungen an Speicherobjekten erst dann dauerhaft vorgenommen werden, wenn Sie **IMAPIProp:: SaveChanges** nach dem letzten **Commit** aufrufen, um das MAPI-Objekt zu speichern. Weitere Informationen finden Sie unter [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).
  
MAPI und COM bieten mehrere API-Funktionen zum Definieren oder zugreifen auf Speicher-und Stream-Objekte. Die häufig verwendeten Funktionen werden in der folgenden Tabelle beschrieben.
  
**Funktionen für den Zugriff auf Speicher-und Stream-Objekte**

|**Funktion**|**Beschreibung**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Erstellt ein Storage-Objekt für den Zugriff auf ein Stream-oder Lock Byte-Objekt.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Erstellt ein Message-Objekt für den Zugriff auf ein Speicherobjekt.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Erstellt ein Stream-Objekt für den Zugriff auf eine Datei.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Erstellt ein Stream-Objekt mit der komprimierten oder nicht komprimierten Version eines Streams, der den Rich-Text einer Nachricht enthält.  <br/> |
   
 **So rufen Sie die Namen der Streams in einem bestimmten unter Speicher ab**
  
1. Rufen Sie die **IStorage:: EnumElements** -Methode des Unterspeichers auf, um eine **IEnumSTATSTG** -Schnittstelle abzurufen. 
    
2. Rufen Sie **IEnumSTATSTG:: Next** mit beliebig vielen **STATSTG** -Strukturen zu einem Zeitpunkt auf. Wenn Sie für 100 gleichzeitig Fragen, gibt **Next** normalerweise S_FALSE zurück, wobei der Inhalt von _pceltFetched_ auf die tatsächlich abgerufene Nummer festgelegt ist. 
    
3. Überprüfen Sie die **STATSTG** -Strukturen, die mit STGTY_STREAM gekennzeichnet sind. 
    
4. Geben Sie den _pwcsName_ -Parameter frei. 
    
 **So erstellen Sie ein Speicherobjekt für den Zugriff auf ein vorhandenes Stream-oder Lock Bytes-Objekt**
  
- Clients rufen [HrIStorageFromStream](hristoragefromstream.md)auf. 
    
 **So erstellen Sie ein Message-Objekt für den Zugriff auf ein vorhandenes Speicherobjekt**
  
- Dienstanbieter und Clients rufen [OpenIMsgOnIStg](openimsgonistg.md)auf. Das erstellte Nachrichtenobjekt unterscheidet sich von den Nachrichtenobjekten, die normalerweise von Nachrichtenspeicher Anbietern erstellt wurden, indem Sie nicht alle [IMessage: IMAPIProp](imessageimapiprop.md) -Schnittstellenmethoden wie **IMessage:: SubmitMessage**. Ein optionaler Eingabeparameter für **OpenIMsgOnIStg** ist eine Rückruffunktion, die dem [MSGCALLRELEASE](msgcallrelease.md) -Prototyp entspricht. Diese Funktion wird vom neuen Message-Objekt aufgerufen, wenn der Verweiszähler der Nachricht 0 (null) erreicht. Das Implementieren einer **MSGCALLRELEASE** -Funktion kann hilfreich sein, um die abschließende Verarbeitung durchzuführen, bevor die neue Nachricht vollständig entfernt wird. 
    
[OpenStreamOnFile](openstreamonfile.md) wird in der Regel zum Speichern von Dateianlagen verwendet, da ein Stream erstellt wird, der aus einer Datei liest und in diese schreibt. **OpenProperty** mit **PR_ATTACH_DATA_BIN** als Property-Tag erstellt einen Stream zum Speichern von binären Anlagendaten. 
  
 **So komprimieren oder Dekomprimieren Sie einen Stream mit Nachrichtentext im Rich-Text-Format**
  
- Clients rufen [WrapCompressedRTFStream](wrapcompressedrtfstream.md)auf. **WrapCompressedRTFStream** erstellt einen Stream, der den RTF-Stream umschließt. Der Wrapper Datenstrom implementiert nicht alle **IStream** -Methoden; die folgenden Methoden sind ausgeschlossen: **Seek**, **SetSize**, **Revert**, **LockRegion**, **UnlockRegion**, **stat**und **Clone**. Dies liegt daran, dass die von **WrapCompressedRTFStream** erstellten Stream-Objekte weder **SetSize** noch **stat**unterstützen, es gibt keine einfache Möglichkeit, ihre Größe zu erweitern oder abzurufen. Die beste Strategie besteht darin, eine angemessene Puffergröße auszuwählen und in einer Schleife zu lesen oder zu schreiben.
    
> [!NOTE]
> COM verfügt über eine Speicherobjekt Implementierung, die auf einem Byte-Array basiert, das ein problematisches **IEnumSTATSTG** -Objekt aus der **EnumElements** -Methode zurückgibt. Insbesondere die **QueryInterface** -Methode funktioniert nicht ordnungsgemäß. Dienstanbieter, die ihre eigenen Speicherobjekte mithilfe der COM-Implementierung implementieren, sollten einen Thin Wrapper für das **IEnumSTATSTG** -Objekt erstellen, das Aufrufe an die zugrunde liegenden **IEnumSTATSTG** -Methoden weiterleitet, aber ein eigenes AddRef implementiert. ** **, **Release**, **QueryInterface**und **Clone** Methoden. 
  

