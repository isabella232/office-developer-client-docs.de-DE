---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406521"
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
  
> [in] Zeiger auf ein Nachrichtensitzungsobjekt, in dem das neue IMessage-on-IStorage-Objekt erstellt werden soll.   
    
_lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
_lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die zum Zuordnen von zusätzlichem Arbeitsspeicher verwendet werden soll. 
    
_lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll. 
    
_lpMalloc_
  
> [in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle verfügbar** machen soll. Die **IMessage-Schnittstelle** muss diese Zuordnungsmethode beim Arbeiten mit Schnittstellen wie **IStorage** und **IStream verwenden.** 
    
_lpMapiSup_
  
> [in] Optionaler Zeiger auf ein MAPI-Unterstützungsobjekt, das ein Dienstanbieter zum Aufrufen der Methoden der [IMAPISupport : IUnknown-Schnittstelle verwenden](imapisupportiunknown.md) kann. 
    
_lpStg_
  
> [in, out] Zeiger auf ein OLE **IStorage-Objekt,** das geöffnet ist und über schreibgeschützte Oder Lese-/Schreibberechtigungen verfügt. Da **IMessage** keinen Schreibzugriff unterstützt, akzeptiert **OpenIMsgOnIStg** kein Speicherobjekt, das im Schreibmodus geöffnet wird. 
    
_lpfMsgCallRelease_
  
> [in] Optionaler Zeiger auf eine Rückruffunktion basierend auf dem [MSGCALLRELEASE-Prototyp,](msgcallrelease.md) den MAPI nach der letzten Version des **IMessage**-on-IStorage-Objekts **aufrufen** soll. 
    
_ulCallerData_
  
> [in] Aufruferdaten, die von MAPI mit dem IMessage-on-IStorage-Objekt **gespeichert** und an die **MSGCALLRELEASE-basierte** Rückruffunktion übergeben werden.  Die Daten bieten Kontext zum **freigegebenen IMessage-Objekt** und zum **IStorage-Objekt,** auf dem es erstellt wurde. 
    
_ulFlags_
  
> [in] Bitmaske von Flags, die verwendet werden, um zu steuern, ob die OLE **IStorage::Commit-Methode** aufgerufen wird, wenn die Clientanwendung oder der Dienstanbieter die **IMessage::SaveChanges-Methode** aufruft. Die folgenden Kennzeichen können festgelegt werden: 
    
IMSG_NO_ISTG_COMMIT 
  
> Die **OLE-Methode IStorage::Commit** darf nicht aufgerufen werden, wenn der Client oder Anbieter [SaveChanges aufruft.](imapiprop-savechanges.md) 
    
MAPI_UNICODE
  
> Ermöglicht das Erstellen von Unicode-MSG-Dateien. Die resultierende [IMessage-Datei](imessageimapiprop.md) STORE_UNICODE_OK in ihrer [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) und unterstützt Unicode-Eigenschaften. 
    
  > [!NOTE]
  > Das MAPI_UNICODE wird nur in dieser Funktion unter Outlook 2003 oder höher unterstützt. 
  
_lppMsg_
  
> [out] Zeiger auf einen Zeiger auf das geöffnete **IMessage-Objekt.** 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Auf Eigenschaftsattribute kann nur auf Eigenschaftsobjekte zugegriffen werden, d. h. auf Objekte, die die [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) implementieren. Um MAPI-Eigenschaften für ein strukturiertes OLE-Speicherobjekt verfügbar zu machen, erstellt **OpenIMsgOnIStg** ein [IMessage : IMAPIProp-Objekt](imessageimapiprop.md) über dem OLE **IStorage-Objekt.** Die Eigenschaftenattribute für solche Objekte können mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) festgelegt oder geändert und mit [GetAttribIMsgOnIStg abgerufen werden.](getattribimsgonistg.md) 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Eine Nachrichtensitzung sollte mit [OpenIMsgSession](openimsgsession.md) geöffnet werden, bevor **OpenIMsgOnIStg** aufgerufen wird. Wenn Sie einen gültigen  _lpMsgSess-Parameter_ angeben, wird sichergestellt, dass die neue Nachricht innerhalb einer Nachrichtensitzung erstellt wird, sodass sie geschlossen wird, wenn die Sitzung geschlossen wird. Wenn  _lpMsgSess_ NULL ist, wird die Nachricht unabhängig von jeder Nachrichtensitzung erstellt. Wenn die Clientanwendung oder der Dienstanbieter, von der die Nachricht erstellt wurde, sie nicht sowie alle Anlagen und geöffneten Tabellen veröffentlicht, ist Arbeitsspeicher nicht mehr verfügbar und kann dazu führen, dass die Anwendung beendet wird. 
  
MAPI verwendet die Funktionen, auf die  _von lpAllocateBuffer_,  _lpAllocateMore_ und  _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und Deallocation, insbesondere zum Zuordnen von Arbeitsspeicher für Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md). Die  _Zeiger lpAllocateBuffer,_  _lpAllocateMore_ und  _lpFreeBuffer_ sind optional, wenn die **OpenIMsgOnIStg-Funktion** mit einem gültigen  _lpMapiSup-Parameter_ aufgerufen wird. 
  
Da es sich um ein zugrunde liegendes OLE-Objekt handelt, muss MAPI auch die OLE-Speicherzuordnung verwenden. Weitere Informationen zu strukturierten OLE-Speicherobjekten und der OLE-Speicherzuweisung finden Sie unter  _OLE Programmer's Reference_. 
  
Wenn ein gültiger Wert für  _lpMapiSup_ angegeben wird, unterstützt **IMessage** die MAPI_DIALOG- und ATTACH_DIALOG-Flags, indem die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) aufruft, um eine Statusbenutzeroberfläche für die [Methoden IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMessage::D eleteAttach](imessage-deleteattach.md) zu liefern. Darüber hinaus versucht die [IMessage::ModifyRecipients-Methode,](imessage-modifyrecipients.md) kurzfristige Eintragsbezeichner durch Aufrufen der [IMAPISupport::OpenAddressBook-Methode](imapisupport-openaddressbook.md) und Aufrufen des resultierenden Adressbuchobjekts in langfristige Eintragsbezeichner zu konvertieren. Wenn NULL für  _lpMapiSup_ übergeben wird, ignoriert **IMessage** MAPI_DIALOG und ATTACH_DIALOG und speichert kurzfristige Eintragsbezeichner ohne Konvertierung. 
  
Das **IStorage-Objekt,** auf das der  _lpStg-Parameter_ verweist, muss entweder im STGM_READ- oder STGM_READWRITE geöffnet werden. Wenn der STGM_READWRITE verwendet wird, muss auch STGM_TRANSACTED festgelegt werden. 
  
Die Rückruffunktion, auf die der  _lpfMsgCallRelease-Parameter_ verweist, ist optional. Sofern angegeben, sollte es auf dem [MSGCALLRELEASE-Funktionsprototyp](msgcallrelease.md) basieren. Die **IMessage-Schnittstelle** ruft sie auf, wenn die Referenzanzahl des IMessage-on-IStorage-Objekts durch den letzten Aufruf der **Release-Methode** auf Null festgelegt ist.   Die Rückruffunktion wird häufig verwendet, um die zugrunde liegende **IStorage-Schnittstelle frei** zu geben. **IMessage** versucht nach dem Rückruf nicht, auf das **IStorage-Objekt** zu zugreifen, auf das der  _lpStg-Parameter_ verweist. 
  
Einige Clients oder Anbieter schreiben möglicherweise zusätzliche Daten in das **IStorage-Objekt** über das hinaus, was **IMessage** selbst schreibt, wenn seine [SaveChanges-Methode](imapiprop-savechanges.md) aufgerufen wird. Der Client oder Anbieter kann das IMSG_NO_ISTG_COMMIT verwenden, um zu verhindern, dass **IMessage** die OLE **IStorage::Commit-Methode** aufruft, während er einen **SaveChanges-Aufruf** verarbeitet. In diesem Fall muss der Client oder Anbieter selbst ein Commit für das **IStorage-Objekt** erstellen, wenn die zusätzlichen Daten geschrieben werden. Um dies zu unterstützen, garantiert die **IMessage-Implementierung,** alle substorages zu benennen, die im **IStorage-Objekt** erstellt werden, beginnend mit der Zeichenfolge "__", d. h. mit zwei Unterstrichen. Der Client oder Anbieter kann Namenskollision vermeiden, indem er seine Unternamen aus diesem Namespace heraushalten. 
  
MAPI definiert nicht das Verhalten mehrerer geöffneter Vorgänge, die für ein Unterobjekt einer Nachricht ausgeführt werden, z. B. eine Anlage, ein Datenstrom oder eine eingebettete Nachricht. MapI ermöglicht derzeit, dass ein bereits geöffnetes Unterobjekt erneut geöffnet wird, aber MAPI führt den open-Vorgang aus, indem die Referenzanzahl für das vorhandene open-Objekt erhöht und an den Client oder Anbieter zurückgezahlt wird, der die [IMessage::OpenAttach-](imessage-openattach.md) oder [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) aufgerufen hat. Dies bedeutet, dass der für den ersten geöffneten Vorgang für ein Unterobjekt angeforderte Zugriff der Zugriff ist, der für alle nachfolgenden geöffneten Vorgänge bereitgestellt wird, unabhängig vom von den Vorgängen angeforderten Zugriff. 
  
Das richtige Verfahren zum Platzieren einer Nachricht in einer Anlage ist das Aufrufen der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) mit dem Schnittstellenbezeichner IID_IMessage. **OpenProperty** unterstützt derzeit auch das Erstellen von Nachrichtenanlagen, die direkt auf der OLE **IStorage-Schnittstelle** verfügbar sind, d. h. mithilfe IID_IStorage Bezeichners. **Der IStorage-Zugriff** wird unterstützt, um eine einfache Möglichkeit zu ermöglichen, ein Microsoft Word-Dokument in eine Anlage zu speichern, ohne es in die **OLE-IStream-Schnittstelle** oder von dieser zu konvertieren. **IMessage** verhält sich jedoch möglicherweise nicht vorhersagbar, wenn **OpenIMsgOnIStg** einen **IStorage-Zeiger** auf die Anlagendaten übergeben wird und die Objekte dann in der falschen Reihenfolge freigegeben werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI verwendet die **OpenIMsgOnIStg-Methode,** um eine IMessage-Schnittstelle über der zu öffnen. MSG-Datei, damit die Datei mit MAPI bearbeitet werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

