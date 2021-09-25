---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: b04095334bbd978938083541eb5550b5e0498a41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595623"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt ein neues [IMessage-Objekt](imessageimapiprop.md) auf einem vorhandenen OLE **IStorage-Objekt,** das in einer Nachrichtensitzung verwendet werden soll. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Imessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und Dienstanbieter  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a>Parameter

_lpMsgSess_
  
> [in] Zeiger auf ein Nachrichtensitzungsobjekt, in dem das neue **IMessage**-on- **IStorage-Objekt** erstellt werden soll. 
    
_lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
_lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die verwendet werden soll, um zusätzlichen Speicher zuzuweisen. 
    
_lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freigeben von Arbeitsspeicher verwendet werden soll. 
    
_lpMalloc_
  
> [in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle** verfügbar machen kann. Die **IMessage-Schnittstelle** muss diese Zuordnungsmethode beim Arbeiten mit Schnittstellen wie **IStorage** und **IStream** verwenden. 
    
_lpMapiSup_
  
> [in] Optionaler Zeiger auf ein MAPI-Unterstützungsobjekt, mit dem ein Dienstanbieter die Methoden der [IMAPISupport : IUnknown-Schnittstelle](imapisupportiunknown.md) aufrufen kann. 
    
_lpStg_
  
> [in, out] Zeiger auf ein geöffnetes OLE **IStorage-Objekt** mit schreibgeschützter Oder Lese-/Schreibberechtigung. Da **IMessage** schreibgeschützten Zugriff nicht unterstützt, akzeptiert **OpenIMsgOnIStg** kein Speicherobjekt, das im schreibgeschützten Modus geöffnet wird. 
    
_lpfMsgCallRelease_
  
> [in] Optionaler Zeiger auf eine Rückruffunktion basierend auf dem [MSGCALLRELEASE-Prototyp,](msgcallrelease.md) den MAPI nach der letzten Version des IMessage-on-IStorage-Objekts aufrufen soll.   
    
_ulCallerData_
  
> [in] Anruferdaten, die von mapi mit dem **IMessage**-on- **IStorage-Objekt** gespeichert und an die **MSGCALLRELEASE-basierte** Rückruffunktion übergeben werden. Die Daten bieten Kontext zu dem **IMessage-Objekt,** das freigegeben wird, und dem **IStorage-Objekt,** auf dem es erstellt wurde. 
    
_ulFlags_
  
> [in] Bitmaske von Flags, die verwendet werden, um zu steuern, ob die OLE **IStorage::Commit-Methode** aufgerufen wird, wenn die Clientanwendung oder der Dienstanbieter die **IMessage::SaveChanges-Methode aufruft.** Die folgenden Flags können festgelegt werden: 
    
IMSG_NO_ISTG_COMMIT 
  
> Die OLE-Methode **IStorage::Commit** wird nicht aufgerufen, wenn der Client oder Anbieter [SaveChanges aufruft.](imapiprop-savechanges.md) 
    
MAPI_UNICODE
  
> Ermöglicht das Erstellen von Unicode-MSG-Dateien. Die resultierende [IMessage-Datei](imessageimapiprop.md) zeigt STORE_UNICODE_OK in ihrer [PR_STORE_SUPPORT_MASK an](pidtagstoresupportmask-canonical-property.md) und unterstützt Unicode-Eigenschaften. 
    
  > [!NOTE]
  > Das flag MAPI_UNICODE wird in dieser Funktion nur ab Outlook 2003 unterstützt. 
  
_lppMsg_
  
> [out] Zeiger auf einen Zeiger auf das geöffnete **IMessage-Objekt.** 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>HinwBemerkungeneise

Auf Eigenschaftsattribute kann nur auf Eigenschaftsobjekte zugegriffen werden, d. h. auf Objekte, die die [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) implementieren. Um MAPI-Eigenschaften für ein strukturiertes OLE-Speicherobjekt verfügbar zu machen, erstellt **OpenIMsgOnIStg** ein [IMessage : IMAPIProp-Objekt](imessageimapiprop.md) über dem OLE **IStorage-Objekt.** Die Eigenschaftsattribute für solche Objekte können mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) festgelegt oder geändert und mit [GetAttribIMsgOnIStg](getattribimsgonistg.md)abgerufen werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Eine Nachrichtensitzung sollte mit [OpenIMsgSession](openimsgsession.md) geöffnet werden, bevor **OpenIMsgOnIStg** aufgerufen wird. Wenn Sie einen gültigen  _lpMsgSess-Parameter_ angeben, stellen Sie sicher, dass die neue Nachricht innerhalb einer Nachrichtensitzung erstellt wird, sodass sie geschlossen wird, wenn die Sitzung geschlossen wird. Wenn  _lpMsgSess_ NULL ist, wird die Nachricht unabhängig von einer Nachrichtensitzung erstellt. Wenn die Clientanwendung oder der Dienstanbieter, von dem die Nachricht erstellt wurde, sie nicht sowie alle anlagen und geöffneten Tabellen freigibt, wird Speicher verloren und kann dazu führen, dass die Anwendung beendet wird. 
  
DIE MAPI verwendet die Funktionen, auf die von _lpAllocateBuffer_, _lpAllocateMore_ und _lpFreeBuffer_ für die meisten Speicherzuweisungen und -zuordnungen verwiesen wird, insbesondere zum Zuordnen von Arbeitsspeicher zur Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows.](imapitable-queryrows.md) Die Zeiger  _lpAllocateBuffer,_  _lpAllocateMore_ und  _lpFreeBuffer_ sind optional, wenn die **OpenIMsgOnIStg-Funktion** mit einem gültigen  _lpMapiSup-Parameter_ aufgerufen wird. 
  
Da es sich um ein zugrunde liegendes OLE-Objekt handelt, muss MAPI auch die OLE-Speicherzuordnung verwenden. Weitere Informationen zu strukturierten OLE-Speicherobjekten und zur OLE-Speicherzuweisung finden Sie in der _OLE-Programmierreferenz._ 
  
Wenn für  _lpMapiSup_ ein gültiger Wert angegeben wird, unterstützt **IMessage** die flags MAPI_DIALOG und ATTACH_DIALOG, indem die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) aufgerufen wird, um eine Status-Benutzeroberfläche für die Methoden [IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMessage::D eleteAttach](imessage-deleteattach.md) anzugeben. Außerdem versucht die [IMessage::ModifyRecipients-Methode,](imessage-modifyrecipients.md) kurzfristige Eintragsbezeichner in langfristige Eintragsbezeichner zu konvertieren, indem sie die [IMAPISupport::OpenAddressBook-Methode](imapisupport-openaddressbook.md) aufruft und Aufrufe des resultierenden Adressbuchobjekts durchführt. Wenn NULL für  _lpMapiSup_ übergeben wird, ignoriert **IMessage** MAPI_DIALOG und ATTACH_DIALOG und speichert kurzfristige Eintragsbezeichner ohne Konvertierung. 
  
Das **IStorage-Objekt,** auf das durch den  _lpStg-Parameter_ verwiesen wird, muss entweder im STGM_READ- oder STGM_READWRITE Modus geöffnet werden. Wenn der STGM_READWRITE Modus verwendet wird, muss auch der STGM_TRANSACTED Modus festgelegt werden. 
  
Die Rückruffunktion, auf die durch den  _Parameter "lpfMsgCallRelease"_ verwiesen wird, ist optional. wenn angegeben, sollte es auf dem Prototyp der [MSGCALLRELEASE-Funktion](msgcallrelease.md) basieren. Die **IMessage-Schnittstelle** ruft sie auf, wenn die Referenzanzahl des IMessage-on-IStorage-Objekts durch den letzten Aufruf der **Release-Methode** auf Null festgelegt ist.   Die Rückruffunktion wird häufig verwendet, um die zugrunde liegende **IStorage-Schnittstelle** frei zu geben. **IMessage** versucht nicht, auf das **IStorage-Objekt** zuzugreifen, auf das der  _lpStg-Parameter_ verweist, nachdem der Rückruf ausgeführt wurde. 
  
Einige Clients oder Anbieter schreiben möglicherweise zusätzliche Daten in das **IStorage-Objekt,** die über das hinausgehen, was **IMessage** selbst schreibt, wenn die [SaveChanges-Methode](imapiprop-savechanges.md) aufgerufen wird. Der Client oder Anbieter kann das flag IMSG_NO_ISTG_COMMIT verwenden, um zu verhindern, dass **IMessage** die **OLE-IStorage::Commit-Methode** aufruft, während ein **SaveChanges-Aufruf** verarbeitet wird. In diesem Fall muss der Client oder Anbieter das **IStorage-Objekt** selbst übernehmen, wenn die zusätzlichen Daten geschrieben werden. Um dies zu unterstützen, garantiert die **IMessage-Implementierung,** alle im **IStorage-Objekt** erstellten Unterteilungen zu benennen, beginnend mit der Zeichenfolge "__", d. h. mit zwei Unterstrichen. Der Client oder Anbieter kann Namenskonflikte vermeiden, indem er seine Unterstoragenamen aus diesem Namespace heraushalten kann. 
  
MapI definiert nicht das Verhalten mehrerer geöffneter Vorgänge, die für ein Unterobjekt einer Nachricht ausgeführt werden, z. B. eine Anlage, ein Datenstrom oder eine eingebettete Nachricht. Die MAPI lässt derzeit zu, dass ein bereits geöffnetes Unterobjekt erneut geöffnet wird. Die MAPI führt jedoch den Vorgang zum Öffnen durch, indem die Referenzanzahl für das vorhandene geöffnete Objekt erhöht und an den Client oder Anbieter zurückgegeben wird, der die [IMessage::OpenAttach-](imessage-openattach.md) oder [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) aufgerufen hat. Dies bedeutet, dass der für den ersten geöffneten Vorgang für ein Unterobjekt angeforderte Zugriff der Zugriff für alle nachfolgenden geöffneten Vorgänge ist, unabhängig vom von den Vorgängen angeforderten Zugriff. 
  
Das richtige Verfahren zum Platzieren einer Nachricht in eine Anlage besteht darin, die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) mit einem Schnittstellenbezeichner von IID_IMessage aufzurufen. **OpenProperty** unterstützt derzeit auch das Erstellen von Nachrichtenanlagen, die direkt auf der OLE **IStorage-Schnittstelle** verfügbar sind, d. h. mithilfe des IID_IStorage Schnittstellenbezeichners. **Der IStorage-Zugriff** wird unterstützt, um eine einfache Möglichkeit zu bieten, ein Microsoft Word Dokument in eine Anlage einzufügen, ohne es in die OLE-IStream-Schnittstelle oder aus der **OLE-IStream-Schnittstelle** zu konvertieren. **IMessage** verhält sich jedoch möglicherweise nicht vorhersagbar, wenn **OpenIMsgOnIStg** ein **IStorage-Zeiger** auf die Anlagendaten übergeben wird und dann die Objekte in der falschen Reihenfolge freigegeben werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI verwendet die **OpenIMsgOnIStg-Methode,** um eine IMessage-Schnittstelle über der . MSG-Datei, damit die Datei mit MAPI bearbeitet werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

