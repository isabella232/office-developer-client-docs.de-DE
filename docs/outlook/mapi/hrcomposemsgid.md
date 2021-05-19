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
  
> [in] Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird. 
    
 _cbStoreRecordKey_
  
> [in] Größe des Datensatzschlüssels des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält, in Bytes. Wenn null im  _cbStoreRecordKey-Parameter_ übergeben wird, zeigt der  _pszMsgID-Parameter_ auf eine Kopie des in Text konvertierten Eintragsbezeichners. 
    
 _pStoreRecordKey_
  
> [in] Zeiger auf den Datensatzschlüssel des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält. 
    
 _cbMsgEID_
  
> [in] Größe des Eintragsbezeichners der Nachricht oder eines anderen Objekts in Bytes. 
    
 _pMsgEID_
  
> [in] Zeiger auf die Eintrags-ID des Objekts. 
    
 _pszMsgID_
  
> [out] Zeiger auf die zurückgegebene ASCII-Zeichenfolge. Wenn der  _cbStoreRecordKey-Parameter_ größer als Null ist, zeigt der  _pszMsgID-Parameter_ auf einen zusammengesetzten Eintragsbezeichner, der in Text konvertiert wurde. Wenn  _cbStoreRecordKey_ null ist,  _zeigt pszMsgID_ auf einen in Text konvertierten Nichtcompound-Eintragsbezeichner. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Wenn sich die Nachricht oder ein anderes Objekt, für das der zusammengesetzte Eintragsbezeichner erstellt wird, in einem Nachrichtenspeicher befindet, wird die Bezeichnerzeichenfolge aus dem Eintragsbezeichner des Objekts und dem Datensatzschlüssel des Speichers erstellt. Wenn sich das Objekt nicht in einem Speicher befindet, d. h. wenn die Byteanzahl für den im  _cbStoreRecordKey-Parameter_ übergebenen Speicherdatensatzschlüssel null ist, wird der Eintragsbezeichner des Objekts einfach kopiert und in eine Zeichenfolge konvertiert. 
  
Das Aufrufen **der HrComposeMsgID-Funktion** entspricht dem Aufrufen der [HrComposeEID-Funktion](hrcomposeeid.md) und dann der [HrSzFromEntryID-Funktion.](hrszfromentryid.md) 
  
 **HrComposeMsgID** ermöglicht Clientanwendungen das Arbeiten mit Objekten in mehreren Speichern mithilfe von zusammengesetzten Eingabebezeichnern. Eine Anwendung kann die [HrDecomposeMsgID-Funktion](hrdecomposemsgid.md) aufrufen, um die zusammengesetzte Eintrags-ID in ihre ursprünglichen Bestandteile zu teilen. 
  

