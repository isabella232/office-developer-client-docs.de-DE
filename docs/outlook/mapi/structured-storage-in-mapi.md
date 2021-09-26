---
title: Strukturierte Storage in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 642a678b-4bf2-4246-85cb-c798de23e36f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: afc817e963a4855aaa5f13ee01b74a82e9ab225e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591031"
---
# <a name="structured-storage-in-mapi"></a>Strukturierte Storage in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Strukturierter Speicher bezieht sich auf die hierarchische Organisation des Speichers, die mit COM eingeführt wurde. In einer strukturierten Speicherumgebung ist der Speicher in zwei oder drei Objekttypen unterteilt: 
  
- Stream-Objekte
    
- Byteobjekte sperren
    
- Storage-Objekte
    
Datenstrom- und Sperrbytes sind Objekte der unteren Ebene, die direkt auf die Daten zugreifen. Stream-Objekte implementieren die **IStream-Schnittstelle,** die Methoden zum Lesen, Schreiben, Positionieren und Kopieren von Bytes von Daten definiert. Lock bytes objects implement another COM interface, **ILockBytes**, to access data with a byte array. Bytearrays werden in der Regel verwendet, um benutzerdefinierten Zugriff auf den zugrunde liegenden Speicher bereitzustellen.
  
Storage Objekte werden über dem Datenstrom übereinander platziert oder Byteobjekte sperren; sie können ein oder mehrere dieser Objekte sowie andere Speicherobjekte enthalten. Storage Objekte implementieren die **IStorage-Schnittstelle,** die Methoden zum Erstellen, Zugreifen und Verwalten geschachtelter Objekte definiert. 
  
Da **IStream,** **ILockBytes** und **IStorage** COM-Schnittstellen anstelle von MAPI-Schnittstellen sind, geben ihre Methoden COM-Fehlerwerte anstelle von MAPI-Werten zurück. Clients und Dienstanbieter, die Methoden in diesen Schnittstellen aufrufen, müssen die API-Funktion **MapStorageSCode** verwenden, um diese Werte in MAPI-Fehlerwerte zu übersetzen. Weitere Informationen finden Sie unter [MapStorageSCode](mapstoragescode.md).
  
Clients und Dienstanbieter verwenden strukturierten Speicher zum Arbeiten mit Eigenschaften, die zu groß für die Verwaltung mit den **IMAPIProp-Methoden** sind, in der Regel große Zeichenfolgen- und binäre Eigenschaften. Eine der gängigen Möglichkeiten für den Zugriff von Clients oder Dienstanbietern ist die Angabe von **IStream** oder **IStorage** als Schnittstellenbezeichner in einem Aufruf der [IMAPIProp::OpenProperty-Methode.](imapiprop-openproperty.md) Clients rufen beispielsweise **OpenProperty** mit **PR_ATTACH_DATA_BIN** als Eigenschaftstag auf und IID_IStream als Schnittstellenbezeichner für den Zugriff auf eine binäre Anlage in einer Nachricht. 
  
Clients und Dienstanbieter können eigene Stream- und Speicherobjekte implementieren oder API-Funktionen aufrufen, um auf von MAPI oder COM bereitgestellte Implementierungen zuzugreifen. Da die bereitgestellten Implementierungen den meisten Zwecken dienen, müssen Clients und Dienstanbieter nur selten eigene erstellen. 
  
Wenn ein Client **OpenProperty** für ein MAPI-Objekt aufruft, um über ein Speicherobjekt auf eine seiner Eigenschaften zuzugreifen, öffnet der Dienstanbieter das Speicherobjekt in der Regel im direkten Modus. Dies ist jedoch ein typisches Verhalten anstelle des erforderlichen Verhaltens. Clients sollten davon ausgehen, dass alle von Dienstanbietern geöffneten oder erstellten Speicherobjekte Transaktionen durchgeführt werden und ein Aufruf von **IStorage::Commit** erforderlich ist. Sie sollten auch bedenken, dass Änderungen an Speicherobjekten erst dauerhaft vorgenommen werden, wenn sie **IMAPIProp::SaveChanges** nach dem letzten **Commit** aufrufen, um das MAPI-Objekt zu speichern. Weitere Informationen finden Sie unter [IMAPIProp::SaveChanges](imapiprop-savechanges.md).
  
MAPI und COM bieten verschiedene API-Funktionen zum Definieren oder Zugreifen auf Speicher- und Streamobjekte. Die häufig verwendeten Funktionen werden in der folgenden Tabelle beschrieben.
  
**Funktionen für den Zugriff auf Storage- und Stream-Objekte**

|**Funktion**|**Beschreibung**|
|:-----|:-----|
|[HrIStorageFromStream](hristoragefromstream.md) <br/> |Erstellt ein Speicherobjekt für den Zugriff auf ein Datenstrom- oder Sperrbyteobjekt.  <br/> |
|[OpenIMsgOnIStg](openimsgonistg.md) <br/> |Erstellt ein Nachrichtenobjekt für den Zugriff auf ein Speicherobjekt.  <br/> |
|[OpenStreamOnFile](openstreamonfile.md) <br/> |Erstellt ein Streamobjekt für den Zugriff auf eine Datei.  <br/> |
|[WrapCompressedRTFStream](wrapcompressedrtfstream.md) <br/> |Erstellt ein Streamobjekt, das die komprimierte oder nicht komprimierte Version eines Datenstroms enthält, der den Rich-Text einer Nachricht enthält.  <br/> |
   
 **So rufen Sie die Namen der Datenströme in einem bestimmten Unterstorage ab**
  
1. Rufen Sie die **IStorage::EnumElements-Methode des Unterstorages** auf, um eine **IEnumSTATSTG-Schnittstelle** abzurufen. 
    
2. Rufen Sie **IEnumSTATSTG::Next** mit beliebig vielen **STATSTG-Strukturen** auf. Wenn Sie jeweils 100 anfordern, gibt **Next** in der Regel S_FALSE zurück, wobei der Inhalt von  _pceltFetched_ auf die Tatsächlich abgerufene Zahl festgelegt ist. 
    
3. Suchen Sie nach den **STATSTG-Strukturen,** die mit STGTY_STREAM gekennzeichnet sind. 
    
4. Geben Sie den  _pwcsName-Parameter_ frei. 
    
 **So erstellen Sie ein Speicherobjekt für den Zugriff auf ein vorhandenes Stream- oder Sperrbyteobjekt**
  
- Clients rufen [HrIStorageFromStream](hristoragefromstream.md)auf. 
    
 **So erstellen Sie ein Nachrichtenobjekt für den Zugriff auf ein vorhandenes Speicherobjekt**
  
- Dienstanbieter und Clients rufen [OpenIMsgOnIStg auf.](openimsgonistg.md) Das erstellte Nachrichtenobjekt unterscheidet sich von den Nachrichtenobjekten, die in der Regel von Nachrichtenspeicheranbietern erstellt werden, insofern, als es nicht alle [IMessage: IMAPIProp-Schnittstellenmethoden](imessageimapiprop.md) unterstützt, z. **B. IMessage::SubmitMessage**. Ein optionaler Eingabeparameter für **OpenIMsgOnIStg** ist eine Rückruffunktion, die dem [MSGCALLRELEASE-Prototyp](msgcallrelease.md) entspricht. Diese Funktion wird vom neuen Nachrichtenobjekt aufgerufen, wenn die Referenzanzahl der Nachricht Null erreicht. Die Implementierung einer **MSGCALLRELEASE-Funktion** kann nützlich sein, um die endgültige Verarbeitung durchzuführen, bevor die neue Nachricht vollständig entfernt wird. 
    
[OpenStreamOnFile](openstreamonfile.md) wird häufig zum Speichern von Dateianlagen verwendet, da ein Datenstrom erstellt wird, der aus einer Datei liest und in eine Datei schreibt. **OpenProperty** mit **PR_ATTACH_DATA_BIN** als Eigenschaftstag erstellt einen Datenstrom zum Speichern binärer Anlagendaten. 
  
 **So komprimieren oder entfernen Sie die Komprimierung eines Datenstroms, der Nachrichtentext im Rich-Text-Format enthält**
  
- Clients rufen [WrapCompressedRTFStream](wrapcompressedrtfstream.md)auf. **WrapCompressedRTFStream** erstellt einen Datenstrom, der den RTF-Stream umschließt. Der Wrapperstream implementiert nicht alle **IStream-Methoden.** Die folgenden Methoden sind ausgeschlossen: **Seek**, **SetSize**, **Revert**, **LockRegion**, **UnlockRegion**, **Stat** und **Clone**. Dies liegt daran, dass die von **WrapCompressedRTFStream** erstellten Streamobjekte **weder SetSize** noch **Stat** unterstützen, gibt es keine einfache Möglichkeit, ihre Größe zu erweitern oder abzurufen. Die beste Strategie besteht darin, eine angemessene Puffergröße zu wählen und in einer Schleife zu lesen oder zu schreiben.
    
> [!NOTE]
> COM verfügt über eine Speicherobjektimplementierungen basierend auf einem Bytearray, das ein **IEnumSTATSTG-Objekt** aus der **problematischen EnumElements-Methode** zurückgibt. Insbesondere funktioniert die **QueryInterface-Methode** nicht ordnungsgemäß. Dienstanbieter, die ihre eigenen Speicherobjekte mithilfe der COM-Implementierung implementieren, sollten einen thin Wrapper für das **IEnumSTATSTG-Objekt** erstellen, das Aufrufe an die zugrunde liegenden **IEnumSTATSTG-Methoden** weiterleitet, aber seine eigenen **AddRef-,** **Release-,** **QueryInterface-** und **Clone-Methoden** implementiert. 
  

