---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 00d2dce81ecb8db1cd69406136b306acc731cc6c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550204"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Funktion, mit der Nachrichteninhalte oder das Format einer Nachricht vorverarbeitet werden.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Transportanbieter  <br/> |
|Definierte Funktion aufgerufen von:  <br/> |MAPI-Spooler  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a>Parameter

 _lpvSession_
  
> [in] Zeiger auf die zu verwendende Sitzung. 
    
 _lpMessage_
  
> [in] Zeiger auf die Nachricht, die vorverarbeitet werden soll. 
    
 _lpAdrBook_
  
> [in] Zeiger auf das Adressbuch, aus dem der Benutzer Empfänger für die Nachricht auswählen soll. 
    
 _lpFolder_
  
> [in, out] Zeiger auf einen Ordner. Bei der Eingabe zeigt der  _parameter lpFolder_ auf den Ordner, der die vorverarbeiteten Nachrichten enthält. Bei der Ausgabe zeigt  _lpFolder_ auf den Ordner, in dem vorverarbeitete Nachrichten platziert wurden. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die verwendet werden soll, um bei Bedarf zusätzlichen Speicher zuzuweisen. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freigeben von Arbeitsspeicher verwendet werden soll. 
    
 _lpcOutbound_
  
> [out] Zeiger auf die Anzahl der Nachrichten im Array, auf die der  _parameter lpppMessage_ verweist. 
    
 _lpppMessage_
  
> [out] Zeiger auf einen Zeiger auf ein Array von Zeigern für vorverarbeitete oder anderweitig generierte Nachrichten. 
    
 _lppRecipList_
  
> [out] Zeiger auf eine optionale [zurückgegebene ADRLIST-Struktur,](adrlist.md) die vom Präprozessor erkannte Empfänger auflistet, für die die Nachricht nicht zustellbar ist. Weitere Informationen zum Inhalt dieser Liste finden Sie unter der [IMAPISupport::StatusRecips-Methode.](imapisupport-statusrecips.md) 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Nachrichteninhalte wurden erfolgreich vorverarbeitet.
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein Transportanbieter-Nachrichtenpräprozessor kann während der Nachrichtenvorverarbeitung eine Statusanzeige darstellen. Es sollte jedoch niemals ein Dialogfeld vorhanden sein, in dem benutzerinteraktion während der Vorverarbeitung von Nachrichten erforderlich ist. 
  
Wenn ein Präprozessor einer ausgehenden Nachricht große Datenmengen hinzufügt, sollten bestimmte Verfahren befolgt werden. Diese Art von Nachricht kann in einem serverbasierten Nachrichtenspeicher gespeichert werden, wodurch der Präprozessor auf einen Remotespeicher zugreift, was eine zeitaufwändige Prozedur ist. Um dies zu vermeiden, sollte der Präprozessor über eine Option verfügen, die es ihm ermöglicht, Daten zu speichern, die einen großen Speicherplatz in einem lokalen Nachrichtenspeicher belegen, und einen Verweis auf diesen lokalen Speicher in der Nachricht bereitzustellen. 
  
Der Präprozessor sollte keines der Objekte freigeben, die ursprünglich an die **PreprocessMessage-basierte** Funktion übergeben wurden. 
  
Bevor der MAPI-Spooler eine **PreprocessMessage-Funktion** aufrufen kann, muss der Transportanbieter die Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor-Methode](imapisupport-registerpreprocessor.md) registriert haben. Nach dem Aufrufen einer **PreprocessMessage-Funktion** kann der Spooler die Übermittlung einer Nachricht erst fortsetzen, wenn die Funktion zurückgegeben wird. 
  
Der MAPI-Spooler besitzt die Aufgabe, Nachrichten zu senden. Dies bedeutet, dass die ursprüngliche Nachricht nie in einem Array von Nachrichtenzeigern platziert wird und dass niemals ein Aufruf der **SubmitMessage-Methoden** erforderlich ist. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

