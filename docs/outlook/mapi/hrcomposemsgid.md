---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424063"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine ASCII-Zeichenfolge, die eine verknüpfte Eintrags-ID für ein Objekt darstellt, in der Regel eine Nachricht in einem Nachrichtenspeicher. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a>Parameter

 _psession_
  
> in Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird. 
    
 _cbStoreRecordKey_
  
> in Größe (in Bytes) des Daten Satz Schlüssels des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält. Wenn NULL im _cbStoreRecordKey_ -Parameter übergeben wird, zeigt der _pszMsgID_ -Parameter auf eine Kopie der Eintrags-ID, die in Text konvertiert wurde. 
    
 _pStoreRecordKey_
  
> in Zeiger auf den Datensatzschlüssel des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält. 
    
 _cbMsgEID_
  
> in Größe (in Bytes) der Eintrags-ID der Nachricht oder eines anderen Objekts. 
    
 _pMsgEID_
  
> in Zeiger auf die Eintrags-ID des Objekts. 
    
 _pszMsgID_
  
> Out Zeiger auf die zurückgegebene ASCII-Zeichenfolge. Wenn der _cbStoreRecordKey_ -Parameter größer als NULL ist, zeigt der _pszMsgID_ -Parameter auf eine verknüpfte Eintrags-ID, die in Text konvertiert wurde. Wenn _cbStoreRecordKey_ ist, verweist _pszMsgID_ auf eine nicht zusammengesetzte Eintrags-ID, die in Text konvertiert wurde. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Bemerkungen

Wenn die Nachricht oder ein anderes Objekt, für das die verknüpfte Eintrags-ID erstellt wird, in einem Nachrichtenspeicher gespeichert ist, wird die ID-Zeichenfolge aus der Eintrags-ID des Objekts und dem Record-Schlüssel des Speichers erstellt. Wenn sich das Objekt nicht in einem Speicher befindet, das heißt, wenn die Bytezahl für den im _cbStoreRecordKey_ -Parameter übergebenen Speicher Eintragsschlüssel 0 (null) ist, wird die Eintrags-ID des Objekts einfach kopiert und in eine Zeichenfolge konvertiert. 
  
Das Aufrufen der **HrComposeMsgID** -Funktion entspricht dem Aufrufen der [HrComposeEID](hrcomposeeid.md) -Funktion und dann der [HrSzFromEntryID](hrszfromentryid.md) -Funktion. 
  
 Mit **HrComposeMsgID** können Clientanwendungen mit Objekten in mehreren speichern arbeiten, die mit verknüpften Eingabe Bezeichnern verwendet werden. Eine Anwendung kann die [HrDecomposeMsgID](hrdecomposemsgid.md) -Funktion aufrufen, um den verknüpften Eintragsbezeichner in seine ursprünglichen Bestandteile aufzuteilen. 
  

