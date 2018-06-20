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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 418ffdd19412dcf948d36a5e7df33f7978d0df3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791899"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**Betrifft**: Outlook 
  
Erstellt eine ASCII-Zeichenfolge, die eine zusammengesetzter Eintrags-ID für ein Objekt, das in der Regel eine Meldung in einem Nachrichtenspeicher darstellt. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
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
  
> [in] Zeiger auf die Sitzung von der Clientanwendung verwendet. 
    
 _cbStoreRecordKey_
  
> [in] Größe in Bytes des Schlüssels Datensatz des Nachrichtenspeichers, die die Nachricht oder eines anderen Objekts enthält. Wenn 0 (null) im _CbStoreRecordKey_ -Parameter übergeben wird, wird der _PszMsgID_ Parameter verweist auf eine Kopie des Eintrags-ID in Text konvertiert. 
    
 _pStoreRecordKey_
  
> [in] Zeiger auf den Eintrag Schlüssel des Nachrichtenspeichers, die die Nachricht oder eines anderen Objekts enthält. 
    
 _cbMsgEID_
  
> [in] Größe des Eintrags-ID der Nachricht oder eines anderen Objekts in Bytes. 
    
 _pMsgEID_
  
> [in] Zeiger auf die Eintrags-ID des Objekts. 
    
 _pszMsgID_
  
> [out] Zeiger auf die zurückgegebene ASCII-Zeichenfolge. Wenn der Parameter _CbStoreRecordKey_ größer als NULL ist, wird der _PszMsgID_ Parameter verweist auf ein zusammengesetzter Eintrags-ID in Text konvertiert. Wenn _CbStoreRecordKey_ gleich NULL ist, _PszMsgID_ verweist auf eine noncompound Eintrags-ID in Text konvertiert. 
    
## <a name="return-value"></a>Rückgabewert

None.
  
## <a name="remarks"></a>Hinweise

Wenn die Nachricht oder eines anderen Objekts für die die zusammengesetzter Eintrags-ID erstellt wird, wird in einem Nachrichtenspeicher befindet, wird die Bezeichnerzeichenfolge aus Eintrags-ID für das Objekt und den Store-Eintrag Schlüssel erstellt. Ist das Objekt nicht in einem Speicher, d. h., ist wenn die Byteanzahl für den Store-Eintrag Schlüssel in der _CbStoreRecordKey_ -Parameter übergeben NULL ist, ist Eintrags-ID für das Objekt einfach kopiert und in eine Zeichenfolge konvertiert. 
  
Aufrufen der Funktion **HrComposeMsgID** entspricht dem Aufrufen der [HrComposeEID](hrcomposeeid.md) und klicken Sie dann die Funktion [HrSzFromEntryID](hrszfromentryid.md) . 
  
 **HrComposeMsgID** von Clientanwendungen-Objekte in mehreren Informationsspeichern mithilfe von zusammengesetzten-Eintragsbezeichner entwickelt. Eine Anwendung kann die [HrDecomposeMsgID](hrdecomposemsgid.md) -Funktion, um die zusammengesetzter Eintrags-ID in seiner ursprünglichen Bestandteile aufgeteilt aufrufen. 
  

