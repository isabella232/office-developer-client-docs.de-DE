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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 27a5978d85cf06a31f583b82cd39d0001852876b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793308"
---
# <a name="openimsgonistg"></a>OpenIMsgOnIStg

**Betrifft**: Outlook 
  
Erstellt ein neues [IMessage](imessageimapiprop.md) -Objekt auf der Basis ein vorhandenes OLE **IStorage** -Objekt in einer Nachricht Sitzung verwendet werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen und -Dienstanbieter  <br/> |
   
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
  
> [in] Zeiger auf ein Objekt "Message" Sitzung innerhalb dessen ist die neue **IMessage**- auf - **IStorage** -Objekt erstellt werden soll. 
    
_lpAllocateBuffer_
  
> [in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll. 
    
_lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden. 
    
_lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben. 
    
_lpMalloc_
  
> [in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE **IMalloc** -Schnittstelle verfügbar macht. Die **IMessage** -Schnittstelle muss beim Arbeiten mit Schnittstellen wie **IStorage** und **IStream**diese Zuordnungsmethode verwenden. 
    
_lpMapiSup_
  
> [in] Optionaler Zeiger auf ein MAPI-Support-Objekt, das ein Dienstanbieter verwenden kann, die Methoden des Aufrufen der [IMAPISupport: IUnknown](imapisupportiunknown.md) Schnittstelle. 
    
_lpStg_
  
> [in, out] Zeiger auf ein OLE- **IStorage** -Objekt, das geöffnet ist und hat schreibgeschützte oder Lese-/Schreibberechtigung. Da **IMessage** lesegeschützt nicht unterstützt werden, akzeptiert **OpenIMsgOnIStg** kein Speicherobjekt im Schreibzugriff-Modus geöffnet. 
    
_lpfMsgCallRelease_
  
> [in] Optional Zeiger auf eine Rückruffunktion, die basierend auf den [MSGCALLRELEASE](msgcallrelease.md) Prototyp, die MAPI nach der letzten Version für die **IMessage**- auf - **IStorage** -Objekt aufrufen. 
    
_ulCallerData_
  
> [in] Anrufer-Daten von MAPI mit dem **IMessage**- auf - **IStorage** -Objekt gespeichert und an die **MSGCALLRELEASE** übergebenen basieren Callback-Funktion. Die Daten enthält Kontext zu den **IMessage** -Objekts, das freigegeben und das **IStorage** -Objekt auf der Basis, das es erstellt wurde. 
    
_ulFlags_
  
> [in] Bitmaske von Flags Steuerelement, ob die OLE- **IStorage::Commit** -Methode aufgerufen wird, wenn die Clientanwendung oder -Dienstanbieter die **IMessage::SaveChanges** -Methode aufruft. Die folgenden Kennzeichen können festgelegt werden: 
    
IMSG_NO_ISTG_COMMIT 
  
> Die OLE-Methode **IStorage::Commit** darf nicht aufgerufen werden, wenn der Client oder Anbieter [SaveChanges](imapiprop-savechanges.md)aufruft. 
    
PARAMETER MAPI_UNICODE
  
> Ermöglicht die Erstellung von Unicode-MSG-Dateien. Die resultierende [IMessage](imessageimapiprop.md) Datei zeigt STORE_UNICODE_OK in seiner [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) und Unicode-Eigenschaften unterstützt. 
    
  > [!NOTE]
  > Die Option MAPI_UNICODE wird nur in dieser Funktion auf Outlook 2003 oder höher unterstützt. 
  
_lppMsg_
  
> [out] Zeiger auf einen Zeiger auf das geöffnete **IMessage** -Objekt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Eigenschaftsattribute nur auf Property-Objekte, d. h., durch Implementieren Objekte zugegriffen werden können die [IMAPIProp: IUnknown](imapipropiunknown.md) Schnittstelle. MAPI-Eigenschaften für ein OLE-Objekt strukturierter Speicher zur Verfügung zu stellen, **OpenIMsgOnIStg** erstellt eine [IMessage: IMAPIProp](imessageimapiprop.md) Objekt auf der Basis der OLE- **IStorage** -Objekt. Die Eigenschaftenattribute für solche Objekte können festgelegt oder mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) geändert und mit [GetAttribIMsgOnIStg](getattribimsgonistg.md)abgerufen werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Eine Sofortnachrichtensitzung sollte mit [OpenIMsgSession](openimsgsession.md) geöffnet werden, bevor **OpenIMsgOnIStg** aufgerufen wird. Einen gültigen _LpMsgSess_ -Parameter stellen mit Sures, dass die neue Nachricht wird innerhalb einer Sofortnachrichtensitzung erstellt, sodass es geschlossen wird, wenn die Sitzung beendet wird. Wenn _LpMsgSess_ NULL ist, wird die Nachricht unabhängig von einer Nachricht Sitzung erstellt. Wenn der Clientanwendung oder Dienstanbieter, die die Nachricht erstellt nicht, er als auch alle zugehörigen Anlagen freigegeben und Tabellen öffnen, Arbeitsspeicher ist verloren und beenden die Anwendung verursachen. 
  
MAPI verwendet, die auf den _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ für die meisten Zuweisung von virtuellem Speicher und zur Freigabe, insbesondere für die Verwendung von Clientanwendungen Speicher beim Aufruf von Schnittstellen, um Funktionen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md). Die _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ Zeiger sind optional, wenn die Funktion **OpenIMsgOnIStg** mit einem gültigen _LpMapiSup_ Parameter aufgerufen wird. 
  
Da Umgang mit einem zugrunde liegenden OLE-Objekt muss MAPI auch OLE Zuweisung von virtuellem Speicher verwenden. Weitere Informationen zu OLE-strukturierte Speicherobjekte und OLE-arbeitsspeicherreservierung, finden Sie unter der _OLE Programmer's Reference_. 
  
Wenn Sie ein gültiger Wert für _LpMapiSup_angegeben ist, unterstützt **IMessage** die Flags MAPI_DIALOG und ATTACH_DIALOG durch Aufrufen der [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) -Methode, um eine Benutzeroberfläche für die [IMAPIProp::CopyTo](imapiprop-copyto.md) bereitzustellen und [IMessage::DeleteAttach](imessage-deleteattach.md) -Methoden. Darüber hinaus versucht die [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode, kurzfristige-Eintragsbezeichner durch Aufrufen der [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) -Methode und tätigen von Anrufen auf das resultierende Address Book-Objekt in langfristige-Eintragsbezeichner zu konvertieren. **Wenn NULL für _LpMapiSup_übergeben wird, ignoriert MAPI_DIALOG und ATTACH_DIALOG IMessageund kurzfristige-Eintragsbezeichner ohne Konvertierung speichert.** 
  
Das **IStorage** -Objekt, das durch den Parameter _LpStg_ auf muss in der Beispielcodezeilen oder Accessor-Modus geöffnet werden. Wenn der Accessor-Modus verwendet wird, muss auch der STGM_TRANSACTED Modus festgelegt werden. 
  
Auf den der _LpfMsgCallRelease_ -Parameter die Callback-Funktion ist optional. Wenn dieser Parameter sollte es für den [MSGCALLRELEASE](msgcallrelease.md) Funktionsprototyp basieren. Die **IMessage** -Schnittstelle wird aufgerufen, wenn die Anzahl der Verweise des **IStorage** **IMessage**- auf - Objekts durch den letzten Aufruf die **Release** -Methode NULL festgelegt ist. Die Callback-Funktion wird meist die zugrunde liegende **IStorage** -Schnittstelle frei. **IMessage** wird nicht versucht, auf das **IStorage** -Objekt, das durch den Parameter _LpStg_ nach dem Ändern des Rückrufs auf zugreifen. 
  
Einige Clients oder Anbieter möglicherweise zusätzliche Daten schreiben auf das **IStorage** -Objekt über welche **IMessage** selbst schreibt die [SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen wird. Der Client oder Anbieter können das Flag IMSG_NO_ISTG_COMMIT **IMessage** verhindern, dass die OLE- **IStorage::Commit** -Methode aufrufen, während der Verarbeitung eines Anrufs **SaveChanges** . In diesem Fall muss der Client oder Anbieter selbst **IStorage** -Objekt Wenn ein commit für die zusätzlichen Daten geschrieben werden. Um dies zu erleichtern, garantiert die Implementierung **IMessage** nennen Sie alle Substorages im beginnend mit der Zeichenfolge "_", d. h., mit zwei unterstrichen **IStorage** -Objekt erstellt wird. Der Client oder Anbieter kann Namenskonflikte vermeiden, indem Sie seine Substorage Namen aus diesem Namespace beibehalten. 
  
MAPI definiert nicht das Verhalten von mehreren open-Vorgängen für eine-Unterobjekt einer Nachricht, wie eine Anlage, einen Datenstrom oder eingebettete Nachricht ausgeführt. MAPI ermöglicht derzeit ein Unterobjekt, die noch einmal geöffnet werden geöffnet ist, aber MAPI führt des Vorgangs zum Öffnen, indem erhöht den Referenzzähler für das vorhandene Objekt öffnen und sie an den Client oder Anbieter, die die [IMessage::OpenAttach aufgerufen ](imessage-openattach.md)oder [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode. Dies bedeutet, dass der angeforderte für den ersten Vorgang zum Öffnen einer Unterobjekts Zugriff den Zugriff für alle nachfolgenden open Operationen, unabhängig von der durch die Vorgänge angeforderte Zugriff bereitgestellt wird. 
  
Das Verfahren für die Platzierung einer Nachricht in einer Anlage lautet die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode mit der ID Schnittstelle IID_IMessage aufrufen. **OpenProperty** unterstützt derzeit auch Erstellung von Nachrichtenanlagen verfügbar direkt auf die OLE- **IStorage** -Schnittstelle, d. h., mithilfe des Bezeichners für IID_IStorage-Schnittstelle. **IStorage** Access wird unterstützt, um eine einfache Möglichkeit, ein Microsoft Word-Dokument in eine Anlage zu versetzen, ohne Sie zu konvertieren zu oder von der OLE- **IStream** -Schnittstelle zu ermöglichen. Allerdings **IMessage** vorhersehbar verhält sich möglicherweise nicht **OpenIMsgOnIStg** einen **IStorage** Zeiger auf die Anlagendaten übergeben, und klicken Sie dann die Objekte in der falschen Reihenfolge freigegeben werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|File.cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI (engl.) verwendet die **OpenIMsgOnIStg** -Methode zum Öffnen einer IMessage-Schnittstelle, über die. MSG-Datei so, dass die Datei mit MAPI bearbeitet werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

