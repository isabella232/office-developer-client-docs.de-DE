---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2f0f4321a36bca1b2b93a1e40b74892867ecee47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584528"
---
# <a name="hrcomposemsgid"></a>HrComposeMsgID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine ASCII-Zeichenfolge, die einen zusammengesetzten Eintragsbezeichner für ein Objekt darstellt, in der Regel eine Nachricht in einem Nachrichtenspeicher. 
  
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
  
> [in] Zeiger auf die von der Clientanwendung verwendete Sitzung. 
    
 _cbStoreRecordKey_
  
> [in] Größe des Datensatzschlüssels des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält, in Byte. Wenn null im  _cbStoreRecordKey-Parameter_ übergeben wird, zeigt der  _parameter pszMsgID_ auf eine Kopie des Eintragsbezeichners, der in Text konvertiert wurde. 
    
 _pStoreRecordKey_
  
> [in] Zeiger auf den Datensatzschlüssel des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält. 
    
 _cbMsgEID_
  
> [in] Größe des Eintragsbezeichners der Nachricht oder eines anderen Objekts in Bytes. 
    
 _pMsgEID_
  
> [in] Zeiger auf den Eintragsbezeichner des Objekts. 
    
 _pszMsgID_
  
> [out] Zeiger auf die zurückgegebene ASCII-Zeichenfolge. Wenn der  _parameter cbStoreRecordKey_ größer als Null ist, zeigt der  _parameter pszMsgID_ auf einen zusammengesetzten Eintragsbezeichner, der in Text konvertiert wird. Wenn  _cbStoreRecordKey_ null ist, zeigt  _pszMsgID_ auf einen nicht kompatiblen Eintragsbezeichner, der in Text konvertiert wird. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn sich die Nachricht oder das andere Objekt, für das der zusammengesetzte Eintragsbezeichner erstellt wird, in einem Nachrichtenspeicher befindet, wird die Bezeichnerzeichenfolge anhand des Eintragsbezeichners des Objekts und des Datensatzschlüssels des Speichers erstellt. Wenn sich das Objekt nicht in einem Speicher befindet, d. h. wenn die Byteanzahl für den im  _cbStoreRecordKey-Parameter übergebenen_ Speicherdatensatzschlüssel null ist, wird der Eintragsbezeichner des Objekts einfach kopiert und in eine Zeichenfolge konvertiert. 
  
Das Aufrufen der **HrComposeMsgID-Funktion** entspricht dem Aufrufen der [HrComposeEID-Funktion](hrcomposeeid.md) und dann der [HrSzFromEntryID-Funktion.](hrszfromentryid.md) 
  
 **HrComposeMsgID** ermöglicht Clientanwendungen das Arbeiten mit Objekten in mehreren Speichern mithilfe von zusammengesetzten Eintragsbezeichnern. Eine Anwendung kann die [HrDecomposeMsgID-Funktion](hrdecomposemsgid.md) aufrufen, um den zusammengesetzten Eintragsbezeichner in seine ursprünglichen Bestandteile aufzuteilen. 
  

