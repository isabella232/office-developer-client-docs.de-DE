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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429047"
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
  
> [in] Zeiger auf die Sitzung, die von der Clientanwendung verwendet wird. 
    
 _cbStoreRecordKey_
  
> [in] Größe des Datensatzschlüssels des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält, in Bytes. Wenn null im  _cbStoreRecordKey-Parameter_ übergeben wird, zeigt der  _ppEID-Parameter_ auf eine Kopie des Eintragsbezeichners des Objekts. 
    
 _pStoreRecordKey_
  
> [in] Zeiger auf den Datensatzschlüssel des Nachrichtenspeichers, der die Nachricht oder ein anderes Objekt enthält. 
    
 _cbMsgEID_
  
> [in] Größe des Eintragsbezeichners der Nachricht oder eines anderen Objekts in Bytes. 
    
 _pMsgEID_
  
> [in] Zeiger auf die Eintrags-ID des Objekts. 
    
 _pcbEID_
  
> [out] Zeiger auf die Größe des zurückgegebenen Bezeichners in Bytes. 
    
 _ppEID_
  
> [out] Zeiger auf einen Zeiger auf die zurückgegebene Eintrags-ID. Wenn der Wert des  _cbStoreRecordKey-Parameters_ größer als Null ist, zeigt der  _ppEID-Parameter_ auf einen Zeiger auf den zusammengesetzten Eintragsbezeichner, der erstellt wird. Wenn  _cbStoreRecordKey_ null ist,  _zeigt ppEID_ auf einen Zeiger auf eine Kopie des Eintragsbezeichners des Objekts. 
    
## <a name="return-value"></a>Return value

Keine.
  
## <a name="remarks"></a>Hinweise

Wenn sich die Nachricht oder ein anderes Objekt, für das der zusammengesetzte Eintragsbezeichner erstellt wird, in einem Nachrichtenspeicher befindet, wird der Bezeichner aus dem Eintragsbezeichner des Objekts und dem Datensatzschlüssel des Speichers erstellt. Wenn sich das Objekt nicht in einem Speicher befindet, d. h. wenn die Byteanzahl für den in  _cbStoreRecordKey_ übergebenen Speicherdatensatzschlüssel null ist, wird der Eintragsbezeichner des Objekts einfach kopiert. 
  
Die **HrComposeEID-Funktion** ermöglicht Anwendungen das Arbeiten mit Objekten in mehreren Speichern mithilfe von zusammengesetzten Eingabebezeichnern. Eine Anwendung kann die [HrDecomposeEID-Funktion](hrdecomposeeid.md) aufrufen, um die zusammengesetzte Eintrags-ID in ihre ursprünglichen Bestandteile zu teilen. 
  
## <a name="see-also"></a>Siehe auch



[HrComposeMsgID](hrcomposemsgid.md)
  
[HrDecomposeMsgID](hrdecomposemsgid.md)

