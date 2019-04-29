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
  
Erstellt ein neues [IMessage](imessageimapiprop.md) -Objekt über einem vorhandenen OLE- **IStorage** -Objekt, das in einer nachrichtensitzung verwendet werden soll. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |IMessage. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen und Dienstanbieter  <br/> |
   
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
  
> in Zeiger auf ein Nachrichten Sitzungsobjekt, in dem das neue **IMessage**-on- **IStorage** -Objekt erstellt werden soll. 
    
_lpAllocateBuffer_
  
> in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll. 
    
_lpAllocateMore_
  
> in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll. 
    
_lpFreeBuffer_
  
> in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben. 
    
_lpMalloc_
  
> in Zeiger auf ein Speicher Reservierungs Objekt, das die OLE **IMalloc** -Schnittstelle verfügbar macht. Die **IMessage** -Schnittstelle muss diese Zuordnungsmethode beim Arbeiten mit Schnittstellen wie **IStorage** und **IStream**verwenden. 
    
_lpMapiSup_
  
> in Optionaler Zeiger auf ein MAPI-Unterstützungsobjekt, mit dem ein Dienstanbieter die Methoden der [IMAPISupport: IUnknown](imapisupportiunknown.md) -Schnittstelle aufrufen kann. 
    
_lpStg_
  
> [in, out] Zeiger auf ein OLE- **IStorage** -Objekt, das geöffnet ist und über Leseberechtigung oder Lese-/Schreibzugriff verfügt. Da **IMessage** keinen schreibgeschützten Zugriff unterstützt, akzeptiert **OpenIMsgOnIStg** kein im schreibgeschützten Modus geöffnetes Speicherobjekt. 
    
_lpfMsgCallRelease_
  
> in Optionaler Zeiger auf eine Rückruffunktion basierend auf dem [MSGCALLRELEASE](msgcallrelease.md) -Prototyp, den MAPI nach der letzten Freigabe des **IMessage**-on- **IStorage** -Objekts aufrufen soll. 
    
_ulCallerData_
  
> in Von MAPI gespeicherte Anrufer-Daten mit dem **IMessage**-on- **IStorage** -Objekt und an die **MSGCALLRELEASE** -basierte Rückruffunktion übergeben. Die Daten bieten Kontext über das **IMessage** -Objekt, das freigegeben wird, und das **IStorage** -Objekt, auf dem es erstellt wurde. 
    
_ulFlags_
  
> in Bitmaske der Flags, mit denen gesteuert wird, ob die OLE **IStorage:: Commit** -Methode aufgerufen wird, wenn die Clientanwendung oder der Dienstanbieter die **IMessage:: SaveChanges** -Methode aufruft. Die folgenden Flags können festgelegt werden: 
    
IMSG_NO_ISTG_COMMIT 
  
> Die OLE-Methode **IStorage:: Commit** kann nicht aufgerufen werden, wenn der Client oder Anbieter [SaveChanges](imapiprop-savechanges.md)aufruft. 
    
MAPI_UNICODE
  
> Ermöglicht die Erstellung von Unicode-msg-Dateien. Die resultierende [IMessage](imessageimapiprop.md) -Datei zeigt STORE_UNICODE_OK in der [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) und unterstützt Unicode-Eigenschaften. 
    
  > [!NOTE]
  > Das MAPI_UNICODE-Flag wird nur in dieser Funktion in Outlook 2003 oder höher unterstützt. 
  
_lppMsg_
  
> Out Zeiger auf einen Zeiger auf das geöffnete **IMessage** -Objekt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Auf Eigenschaftsattribute kann nur über Property-Objekte zugegriffen werden, also auf Objekte, die die [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle implementieren. Um MAPI-Eigenschaften für ein OLE Structured Storage-Objekt verfügbar zu machen, erstellt **OpenIMsgOnIStg** ein [IMessage: IMAPIProp](imessageimapiprop.md) -Objekt über dem OLE- **IStorage** -Objekt. Die Eigenschaftsattribute für solche Objekte können mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) festgelegt oder geändert und mit [GetAttribIMsgOnIStg](getattribimsgonistg.md)abgerufen werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Eine nachrichtensitzung sollte mit [OpenIMsgSession](openimsgsession.md) geöffnet werden, bevor **OpenIMsgOnIStg** aufgerufen wird. Durch Angeben eines gültigen _lpMsgSess_ -Parameters stellen Sie sicher, dass die neue Nachricht innerhalb einer nachrichtensitzung erstellt wird, damit Sie geschlossen wird, wenn die Sitzung geschlossen wird. Wenn _lpMsgSess_ ist, wird die Nachricht unabhängig von einer beliebigen nachrichtensitzung erstellt. Wenn die Clientanwendung oder der Dienstanbieter, der die Nachricht erstellt hat, diese nicht freigibt, sowie alle Anhänge und geöffneten Tabellen, wird der Arbeitsspeicher geleckt und kann dazu führen, dass die Anwendung beendet wird. 
  
MAPI verwendet die Funktionen, auf die durch _lpAllocateBuffer_, _lpAllocateMore_und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Aufhebungen, insbesondere für die Zuweisung von Speicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md). Die _lpAllocateBuffer_-, _LpAllocateMore_-und _lpFreeBuffer_ -Zeiger sind optional, wenn die **OpenIMsgOnIStg** -Funktion mit einem gültigen _lpMapiSup_ -Parameter aufgerufen wird. 
  
Da es sich um ein zugrunde liegendes OLE-Objekt handelt, muss MAPI auch die OLE-Speicherbelegung verwenden. Weitere Informationen zu OLE-strukturierten Speicherobjekten und zur OLE-Speicherzuordnung finden Sie unter _OLE Programmer es Reference_. 
  
Wenn für _lpMapiSup_ein gültiger Wert angegeben wird, unterstützt **IMESSAGE** die Flags MAPI_DIALOG und ATTACH_DIALOG durch aufrufen der [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) -Methode, um eine Fortschritts-Benutzeroberfläche für die [IMAPIProp:: CopyTo](imapiprop-copyto.md) bereitzustellen. und [IMessage::D eleteattach](imessage-deleteattach.md) -Methoden. Außerdem versucht die [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode, kurzfristige Eintrags-IDs in langfristige Eintragsbezeichner zu konvertieren, indem die [IMAPISupport:: openaddressbook](imapisupport-openaddressbook.md) -Methode aufgerufen wird und Aufrufe für das resultierende Adressbuchobjekt durchführen. Wenn NULL für _lpMapiSup_übergeben wird, ignoriert **IMESSAGE** MAPI_DIALOG und ATTACH_DIALOG und speichert kurzfristige Eintragsbezeichner ohne Konvertierung. 
  
Das **IStorage** -Objekt, auf das durch den _lpStg_ -Parameter verwiesen wird, muss im STGM_READ-oder STGM_READWRITE-Modus geöffnet werden. Wenn der STGM_READWRITE-Modus verwendet wird, muss auch der STGM_TRANSACTED-Modus festgelegt werden. 
  
Die Rückruffunktion, auf die durch den _lpfMsgCallRelease_ -Parameter verwiesen wird, ist optional; Wenn angegeben, sollte Sie auf dem Prototyp der [MSGCALLRELEASE](msgcallrelease.md) -Funktion basieren. Die **IMessage** -Schnittstelle ruft Sie auf, wenn der Verweiszähler des **IMessage**-on- **IStorage** -Objekts durch den letzten Aufruf seiner **Release** -Methode auf NULL festgelegt ist. Die Callback-Funktion wird häufig verwendet, um die zugrunde liegende **IStorage** -Schnittstelle freizugeben. **IMessage** versucht nicht, auf das **IStorage** -Objekt zuzugreifen, auf das durch den _lpStg_ -Parameter verwiesen wird, nachdem der Rückruf vorgenommen wurde. 
  
Einige Clients oder Anbieter schreiben möglicherweise zusätzliche Daten in das **IStorage** -Objekt, über die **IMessage** selbst hinaus schreibt, wenn die [SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen wird. Der Client oder Anbieter kann das IMSG_NO_ISTG_COMMIT-Flag verwenden, um zu verhindern, dass **IMessage** beim Verarbeiten eines **SaveChanges** -Aufrufs die OLE **IStorage:: Commit** -Methode aufruft. in diesem Fall muss der Client oder Anbieter selbst das **IStorage** -Objekt übertragen, wenn die zusätzlichen Daten geschrieben werden. Um dies zu unterstützen, stellt die **IMessage** -Implementierung sicher, dass alle unter Speicher, die im **IStorage** -Objekt erstellt werden, beginnend mit der Zeichenfolge "__", also mit zwei unterstrichen, benannt werden. Der Client oder Anbieter kann Namenskonflikte vermeiden, indem er seine unter Speichernamen aus diesem Namespace behält. 
  
MAPI definiert nicht das Verhalten mehrerer geöffneter Vorgänge, die für ein Unterobjekt einer Nachricht ausgeführt werden, beispielsweise eine Anlage, einen Datenstrom oder eine eingebettete Nachricht. MAPI ermöglicht derzeit, dass ein Unterobjekt, das bereits geöffnet ist, noch einmal geöffnet wird, aber MAPI führt den Öffnungsvorgang aus, indem er den Verweiszähler für das vorhandene Open-Objekt inkrementiert und an den Client oder Anbieter zurückgibt, der die IMessage:: openAttach-Funktion aufgerufen hat [. ](imessage-openattach.md)oder [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode. Dies bedeutet, dass der für den ersten geöffneten Vorgang für ein Unterobjekt angeforderte Zugriff der Zugriff für alle nachfolgenden geöffneten Vorgänge ist, unabhängig davon, welcher Zugriff von den Vorgängen angefordert wird. 
  
Das richtige Verfahren zum Platzieren einer Nachricht in einer Anlage besteht darin, die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode mit einem Schnittstellenbezeichner von IID_IMessage aufzurufen. **OpenProperty** unterstützt derzeit auch die Erstellung von Nachrichtenanlagen, die direkt auf der OLE- **IStorage** -Schnittstelle verfügbar sind, also mithilfe der IID_IStorage-Schnittstellenkennung. **IStorage** -Zugriff wird unterstützt, um eine einfache Möglichkeit zum Einfügen eines Microsoft Word-Dokuments in eine Anlage zu ermöglichen, ohne Sie in die oder von der OLE **IStream** -Schnittstelle zu konvertieren. **IMessage** reagiert möglicherweise nicht vorhersehbar, wenn **OpenIMsgOnIStg** einen **IStorage** -Zeiger auf die Anlagendaten übergeben wird und die Objekte dann in der falschen Reihenfolge freigegeben werden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|Datei. cpp  <br/> |LoadMSGToMessage  <br/> |MFCMAPI verwendet die **OpenIMsgOnIStg** -Methode, um eine IMessage-Schnittstelle über dem zu öffnen. MSG-Datei, sodass die Datei mit MAPI manipuliert werden kann.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

