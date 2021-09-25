---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ad7152106faaf604f2ea5306fce894a7117a06fa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584556"
---
# <a name="hrcomposeeid"></a>HrComposeEID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt einen zusammengesetzten Eintragsbezeichner für ein Objekt, in der Regel eine Nachricht in einem Nachrichtenspeicher. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiutil.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
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
  
> [in] Zeiger auf die von der Clientanwendung verwendete Sitzung. 
    
 _cbStoreRecordKey_
  
> [in] Größe des Datensatzschlüssels des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält, in Byte. Wenn null im  _cbStoreRecordKey-Parameter_ übergeben wird, zeigt der  _ppEID-Parameter_ auf eine Kopie des Eintragsbezeichners des Objekts. 
    
 _pStoreRecordKey_
  
> [in] Zeiger auf den Datensatzschlüssel des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält. 
    
 _cbMsgEID_
  
> [in] Größe des Eintragsbezeichners der Nachricht oder eines anderen Objekts in Bytes. 
    
 _pMsgEID_
  
> [in] Zeiger auf den Eintragsbezeichner des Objekts. 
    
 _pwEID_
  
> [out] Zeiger auf die Größe des zurückgegebenen Bezeichners in Bytes. 
    
 _ppEID_
  
> [out] Zeiger auf einen Zeiger auf den zurückgegebenen Eintragsbezeichner. Wenn der Wert des  _cbStoreRecordKey-Parameters_ größer als Null ist, zeigt der  _ppEID-Parameter_ auf einen Zeiger auf den zusammengesetzten Eintragsbezeichner, der erstellt wird. Wenn  _cbStoreRecordKey_ null ist, zeigt  _ppEID_ auf einen Zeiger auf eine Kopie des Eintragsbezeichners des Objekts. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn sich die Nachricht oder das andere Objekt, für das der zusammengesetzte Eintragsbezeichner erstellt wird, in einem Nachrichtenspeicher befindet, wird der Bezeichner anhand des Eintragsbezeichners des Objekts und des Datensatzschlüssels des Speichers erstellt. Wenn sich das Objekt nicht in einem Speicher befindet, d. h. wenn die Byteanzahl für den in  _cbStoreRecordKey übergebenen_ Speicherdatensatzschlüssel null ist, wird der Eintragsbezeichner des Objekts einfach kopiert. 
  
Die **HrComposeEID-Funktion** ermöglicht Anwendungen das Arbeiten mit Objekten in mehreren Speichern mithilfe von zusammengesetzten Eintragsbezeichnern. Eine Anwendung kann die [HrDecomposeEID-Funktion](hrdecomposeeid.md) aufrufen, um den zusammengesetzten Eintragsbezeichner in die ursprünglichen Bestandteile aufzuteilen. 
  
## <a name="see-also"></a>Siehe auch



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

