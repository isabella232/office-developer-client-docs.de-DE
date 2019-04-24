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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351380"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Funktion, die den Nachrichteninhalt oder das Format einer Nachricht vorverarbeitet.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |Transport Anbieter  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |MAPI-Spooler  <br/> |
   
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
  
> in Zeiger auf die zu verwendende Sitzung. 
    
 _lpMessage_
  
> in Zeiger auf die Nachricht, die vorverarbeitet werden soll. 
    
 _lpAdrBook_
  
> in Zeiger auf das Adressbuch, aus dem der Benutzer Empfänger für die Nachricht auswählen soll. 
    
 _lpFolder_
  
> [in, out] Zeiger auf einen Ordner. Bei der Eingabe zeigt der Parameter _lpFolder_ auf den Ordner mit Nachrichten, die vorverarbeitet werden sollen. Bei der Ausgabe zeigt _lpFolder_ auf den Ordner, in dem vorverarbeitete Nachrichten abgelegt wurden. 
    
 _lpAllocateBuffer_
  
> in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die verwendet werden soll, um bei Bedarf zusätzlichen Arbeitsspeicher zuzuordnen. 
    
 _lpFreeBuffer_
  
> in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _lpcOutbound_
  
> Out Zeiger auf die Anzahl der Nachrichten im Array, auf die durch den _lpppMessage_ -Parameter verwiesen wird. 
    
 _lpppMessage_
  
> Out Zeiger auf einen Zeiger auf ein Array von Zeigern auf vorverarbeitete oder anderweitig generierte Nachrichten. 
    
 _lppRecipList_
  
> Out Zeiger auf eine optionale zurückgegebene [ADRLIST](adrlist.md) -Struktur, die Vorprozessor-erkannte Empfänger auflistet, für die die Nachricht unzustellbar ist. Weitere Informationen zu den Inhalten dieser Liste finden Sie unter der [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) -Methode. 
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Nachrichteninhalt wurde erfolgreich vorverarbeitet.
    
## <a name="remarks"></a>Bemerkungen

Ein Transportanbieter-Nachrichten Präprozessor kann während der Nachrichten Vorverarbeitung eine Statusanzeige darstellen. Es sollte jedoch nie ein Dialogfeld angezeigt werden, das die Benutzerinteraktion während der Nachrichten Vorverarbeitung erfordert. 
  
Wenn ein Präprozessor große Datenmengen zu einer ausgehenden Nachricht hinzufügt, sollten bestimmte Verfahren befolgt werden. Diese Art von Nachricht kann in einem Server basierten Nachrichtenspeicher gespeichert werden, wodurch der Präprozessor auf einen Remotespeicher zugreift, ein zeitaufwändiger Vorgang. Um dies zu vermeiden, sollte der Präprozessor über eine Option verfügen, die es ermöglicht, Daten zu speichern, die sehr viel Speicherplatz in einem lokalen Nachrichtenspeicher benötigen, und einen Verweis auf diesen lokalen Speicher in der Nachricht bereitzustellen. 
  
Der Präprozessor sollte keines der Objekte freigeben, die ursprünglich an die **PreprocessMessage** -basierte Funktion übergeben wurden. 
  
Bevor der MAPI-Spooler eine **PreprocessMessage** -Funktion aufrufen kann, muss der Transportanbieter die Funktion bei einem Aufruf der [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode registriert haben. Nach dem Aufrufen einer **PreprocessMessage** -Funktion kann der Spooler keine Nachricht mehr senden, bis die Funktion zurückgegeben wird. 
  
Der MAPI-Spooler besitzt die Aufgabe, Nachrichten zu übermitteln. Dies bedeutet, dass die ursprüngliche Nachricht nie in einem Array von Nachrichten Zeigern angeordnet wird, und dass ein Aufruf der **SubmitMessage** -Methoden nie erforderlich ist. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

