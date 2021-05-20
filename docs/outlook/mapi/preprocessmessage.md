---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437245"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Funktion, die Nachrichteninhalte oder das Format einer Nachricht vorverarbeitet.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |Transportanbieter  <br/> |
|Definierte Funktion, die von:  <br/> |MAPI-Spooler  <br/> |
   
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
  
> [in] Zeiger auf die nachricht, die vorverarbeitet werden soll. 
    
 _lpAdrBook_
  
> [in] Zeiger auf das Adressbuch, aus dem der Benutzer Empfänger für die Nachricht auswählen soll. 
    
 _lpFolder_
  
> [in, out] Zeiger auf einen Ordner. Bei der Eingabe zeigt  _der lpFolder-Parameter_ auf den Ordner, der nachrichten enthält, die vorverarbeitet werden sollen. Bei der Ausgabe  _zeigt lpFolder_ auf den Ordner, in dem vorverarbeitete Nachrichten platziert wurden. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die verwendet werden soll, um bei Bedarf zusätzlichen Arbeitsspeicher zuzuordnen. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll. 
    
 _lpcOutbound_
  
> [out] Zeiger auf die Anzahl der Nachrichten im Array, auf die der  _lpppMessage-Parameter_ verweist. 
    
 _lpppMessage_
  
> [out] Zeiger auf einen Zeiger auf ein Array von Zeigern auf vorverarbeitete oder anderweitig generierte Nachrichten. 
    
 _lppRecipList_
  
> [out] Zeiger auf eine optionale zurückgegebene [ADRLIST-Struktur,](adrlist.md) in der vorverarbeitete Empfänger auflistet werden, für die die Nachricht nicht zustellbar ist. Weitere Informationen zum Inhalt dieser Liste finden Sie unter [IMAPISupport::StatusRecips-Methode.](imapisupport-statusrecips.md) 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Nachrichteninhalte wurden erfolgreich vorverarbeitet.
    
## <a name="remarks"></a>Hinweise

Ein Nachrichtenvorprozessor des Transportanbieters kann während der Nachrichtenvorverarbeitung eine Statusanzeige anzeigen. Es sollte jedoch niemals ein Dialogfeld angezeigt werden, das eine Benutzerinteraktion während der Nachrichtenvorverarbeitung erfordert. 
  
Wenn ein Präprozessor einer ausgehenden Nachricht große Datenmengen hinzufügt, sollten bestimmte Verfahren befolgt werden. Diese Art von Nachricht kann in einem serverbasierten Nachrichtenspeicher gespeichert werden, was dazu führt, dass der Präprozessor auf einen Remotespeicher zu zugegriffen hat, was eine zeitaufwändige Prozedur ist. Um dies zu vermeiden, sollte der Präprozessor über eine Option verfügen, mit der Daten gespeichert werden können, die viel Speicherplatz in einem lokalen Nachrichtenspeicher enthalten und einen Verweis auf diesen lokalen Speicher in der Nachricht bereitstellen können. 
  
Der Präprozessor sollte keine der Objekte los, die ursprünglich an die **PreprocessMessage-basierte** Funktion übergeben wurden. 
  
Bevor der MAPI-Spooler eine **PreprocessMessage-Funktion** aufrufen kann, muss der Transportanbieter die Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor-Methode](imapisupport-registerpreprocessor.md) registriert haben. Nach dem Aufrufen **einer PreprocessMessage-Funktion** kann der Spooler die Übermittlung einer Nachricht erst fortsetzen, wenn die Funktion zurückgegeben wird. 
  
Der MAPI-Spooler besitzt die Aufgabe, Nachrichten zu übermitteln. Dies bedeutet, dass die ursprüngliche Nachricht niemals in einem Array von Nachrichtenzeigern platziert wird und kein Aufruf der **SubmitMessage-Methoden** erforderlich ist. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

