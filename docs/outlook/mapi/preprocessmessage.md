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
ms.openlocfilehash: 22562e1177c9a649bc66b25b5e8e9e6ecc8e397c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795310"
---
# <a name="preprocessmessage"></a>PreprocessMessage

  
  
**Betrifft**: Outlook 
  
Definiert eine Funktion, die vorverarbeitet Nachrichteninhalt oder das Format einer Nachricht.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapispi.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |Transportanbieter  <br/> |
|Definierte Funktion aufgerufen:  <br/> |MAPI-Warteschlange  <br/> |
   
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
  
> [in] Zeiger auf die Sitzung verwendet werden. 
    
 _lpMessage_
  
> [in] Zeiger auf die Nachricht vorverarbeitet werden. 
    
 _lpAdrBook_
  
> [in] Zeiger auf das Adressbuch von dem der Benutzer Empfänger der Nachricht wählen sollten. 
    
 _lpFolder_
  
> [in, out] Zeiger in einen Ordner. Zeigt bei der Eingabe der _LpFolder_ -Parameter auf den Ordner, der vorverarbeitet werden Nachrichten enthält. Ausgabe _LpFolder_ zeigt auf den Ordner, in dem vorverarbeitete Nachrichten abgelegt wurden. 
    
 _lpAllocateBuffer_
  
> [in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll. 
    
 _lpAllocateMore_
  
> [in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden, in denen erforderlich. 
    
 _lpFreeBuffer_
  
> [in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben. 
    
 _lpcOutbound_
  
> [out] Zeiger auf die Anzahl der Nachrichten in der Matrix, durch den Parameter _LpppMessage_ auf zeigt. 
    
 _lpppMessage_
  
> [out] Zeiger auf einen Zeiger auf ein Array von Zeigern für vorverarbeitet oder andernfalls Nachrichten generiert. 
    
 _lppRecipList_
  
> [out] Zeiger auf eine optionale zurückgegebenen [ADRLIST](adrlist.md) -Struktur, auflisten Präprozessor erkannt Empfänger für die Nachricht nicht zugestellt werden kann. Weitere Informationen über den Inhalt dieser Liste finden Sie unter der [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Nachrichteninhalt wurden erfolgreich vorverarbeitet.
    
## <a name="remarks"></a>Hinweise

Ein Adressbuchhierarchie Nachricht Präprozessor kann eine Statusanzeige während der vorverarbeitung Nachricht darstellen. Sie sollten jedoch noch nie ein Dialogfeld Benutzereingriff während der vorverarbeitung Nachricht dar. 
  
Wenn ein Präprozessor große Datenmengen eine ausgehende Nachricht hinzufügt, müssen bestimmte Verfahren folgen. Nachrichten dieses Typs kann in einem serverbasierten Nachrichtenspeicher gespeichert werden, verursacht des Präprozessors auf einen remote-Speicher sehr zeitaufwendig zugreifen. Um dies vermeiden möchten, sollte der Präprozessor eine Option, die Ihnen zum Speichern von Daten, die eine große Menge an Speicherplatz in einem lokalen Nachrichtenspeicher akzeptiert, und geben Sie einen Verweis auf diesen lokalen Speicher in der Nachricht ermöglicht. 
  
Der Präprozessor sollte nicht mit den Objekten, die ursprünglich übergeben an die Funktion **PreprocessMessage** basierend freigeben. 
  
Bevor die MAPI-Warteschlange eine **PreprocessMessage** -Funktion aufgerufen werden kann, muss der Adressbuchhierarchie die Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode registriert haben. Nach dem Aufrufen einer Funktion **PreprocessMessage** , kann nicht die Warteschlange weiterhin eine Nachricht senden, bis der Funktion zurückgegeben. 
  
Die MAPI-Warteschlange besitzt die Aufgabe übermitteln von Nachrichten an. Dies bedeutet, dass die ursprüngliche Nachricht nie in ein Array von Zeigern Nachricht befindet und dass ein Anruf an die Methoden **SubmitMessage** nie erforderlich ist. 
  
## <a name="see-also"></a>Siehe auch



[IAddrBook: IMAPIProp](iaddrbookimapiprop.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

