---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348062"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine verknüpfte Eintrags-ID für ein Objekt, in der Regel eine Nachricht in einem Nachrichtenspeicher. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a>Parameter

 _psession_
  
> in Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird. 
    
 _cbStoreRecordKey_
  
> in Größe (in Byte) des Daten Satz Schlüssels des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt hält. Wenn NULL im _cbStoreRecordKey_ -Parameter übergeben wird, zeigt der _ppEID_ -Parameter auf eine Kopie der Eintrags-ID des Objekts. 
    
 _pStoreRecordKey_
  
> in Zeiger auf den Datensatzschlüssel des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält. 
    
 _cbMsgEID_
  
> in Größe (in Bytes) der Eintrags-ID der Nachricht oder eines anderen Objekts. 
    
 _pMsgEID_
  
> in Zeiger auf die Eintrags-ID des Objekts. 
    
 _pcbEID_
  
> Out Zeiger auf die Größe des zurückgegebenen Bezeichners in Byte. 
    
 _ppEID_
  
> Out Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner. Wenn der Wert des _cbStoreRecordKey_ -Parameters größer als NULL ist, zeigt der Parameter _ppEID_ auf einen Zeiger auf den verknüpften Eintragsbezeichner, der erstellt wird. Wenn _cbStoreRecordKey_ ist, verweist _ppEID_ auf einen Zeiger auf eine Kopie des Eintrags Bezeichners des Objekts. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Wenn die Nachricht oder ein anderes Objekt, für das die verknüpfte Eintrags-ID erstellt wird, in einem Nachrichtenspeicher gespeichert ist, wird der Bezeichner aus der Eintrags-ID des Objekts und dem Record-Schlüssel des Speichers erstellt. Wenn sich das Objekt nicht in einem Speicher befindet, das heißt, wenn die Bytezahl für den in _cbStoreRecordKey_ übergebenen Speicher Eintragsschlüssel NULL ist, wird die Eintrags-ID des Objekts einfach kopiert. 
  
Mit der **HrComposeEID** -Funktion können Anwendungen mit Objekten in mehreren speichern mithilfe von verknüpften Eingabe Bezeichnern verwendet werden. Eine Anwendung kann die [HrDecomposeEID](hrdecomposeeid.md) -Funktion aufrufen, um den verknüpften Eintragsbezeichner in seine ursprünglichen Bestandteile aufzuteilen. 
  
## <a name="see-also"></a>Siehe auch



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

