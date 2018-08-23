---
title: IMessageModifyRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.ModifyRecipients
api_type:
- COM
ms.assetid: 2625f29d-325f-417d-bcec-49d580f9cd7e
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0735008575db5e1cab62dbde4b699b15e04cedb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567286"
---
# <a name="imessagemodifyrecipients"></a>IMessage::ModifyRecipients

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Hinzugef�gt, gel�scht oder Empf�nger der Nachricht �ndert.
  
```cpp
HRESULT ModifyRecipients(
  ULONG ulFlags,
  LPADRLIST lpMods
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Bitmaske aus Flags, die die Empfänger Änderungen steuert. Wenn 0 (null) für den _UlFlags_ -Parameter übergeben wird, alle vorhandenen Empfänger von **ModifyRecipients** durch die Empfängerliste auf das durch den Parameter _LpMods_ ersetzt. Die folgenden Kennzeichen können für _UlFlags_festgelegt werden:
    
MODRECIP_ADD 
  
> Die Empf�nger auf die durch den Parameter  _lpMods_ sollte die Empf�ngerliste hinzugef�gt werden. 
    
MODRECIP_MODIFY 
  
> Die Empf�nger auf die durch den Parameter  _lpMods_ sollten bereits vorhandene Empf�nger ersetzen. Alle vorhandenen Eigenschaften werden durch die in der entsprechenden [ADRENTRY](adrentry.md) Struktur ersetzt. 
    
MODRECIP_REMOVE 
  
> Aus der Empfängerliste mithilfe als Index der **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))-Eigenschaft, die im Array Eigenschaft Wert für jeden Empfänger Eintrag in der _LpMods_ -Parameter enthalten sollte bereits vorhandene Empfänger entfernt werden. 
    
 _lpMods_
  
> [in] Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die eine Liste der Empf�nger hinzugef�gt, gel�scht oder ge�ndert werden, in der Nachricht enth�lt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Empf�ngerliste wurde erfolgreich ge�ndert.
    
## <a name="remarks"></a>Hinweise

Die **IMessage::ModifyRecipients** -Methode �ndert die Nachricht Empf�ngerliste. Es ist in dieser Liste gehalten in eine [ADRLIST](adrlist.md) -Struktur, dass die Empf�nger Tabelle erstellt wird. 
  
Die **ADRLIST** -Datenstruktur enth�lt eine [ADRENTRY](adrentry.md) -Struktur f�r jeden Empf�nger und jede **ADRENTRY** -Datenstruktur enth�lt ein Array der Eigenschaftswerte, die die Empf�ngereigenschaften beschreibt. 
  
Empf�nger in der Struktur **ADRLIST** k�nnen gel�st oder nicht aufgel�st werden. Der Unterschied liegt in der Anzahl und Typ der Eigenschaften, die eingebunden werden. Ein nicht aufgelöster Empfänger enthält nur die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)) Eigenschaften während ein aufgelöster Empfänger, die zwei Eigenschaften sowie **PR_ADDRTYPE enthält **([PidTagAddressType](pidtagaddresstype-canonical-property.md)) und **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Wenn **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) zur Verfügung steht, können sie auch berücksichtigt.
  
Durch die Zeit, die eine Nachricht gesendet wird, muss nur aufgel�sten Empf�nger in der Empf�ngerliste enthalten. Nicht aufgel�sten Empf�nger verursachen Unzustellbarkeitsberichten erstellt und an den urspr�nglichen Absender der Nachricht gesendet werden. Weitere Informationen zu den Vorgang der Namensaufl�sung aus Sicht des Clients finden Sie unter [Aufl�sen von Namen](resolving-a-recipient-name.md). Weitere Informationen aus der Perspektive der Adressbuchanbieter finden Sie unter [Implementieren der Namensaufl�sung](implementing-name-resolution.md).
  
Nicht aufgel�st und nicht aufgel�sten Empf�nger kann ein Empf�nger NULL sein. Das **cValues** Mitglied der **ADRENTRY** -Struktur f�r den Empf�nger auf 0 (null) festgelegt ist und der **rgPropVals** Member wird auf NULL festgelegt. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie k�nnen eine Empf�ngerliste durch Aufrufen von [IAddrBook::Address](imapisupport-address.md) zum Anzeigen des Standarddialogfelds und der Benutzer aufgefordert, w�hlen Sie Eintr�ge erstellen. Die Adressliste auf die durch den Parameter  _lppAdrList_ auf **Address** kann an **ModifyRecipients** als  _lpMods_ -Parameter �bergeben werden. 
  
Wenn Sie Eigenschaften f�r einen Empf�nger in der Struktur [ADRLIST](adrlist.md) angeben, schlie�en Sie alle Eigenschaften des Empf�ngers, nicht nur diejenigen neuen oder ge�nderten. Wenn Sie ein Empf�nger ge�ndert wird, werden alle Eigenschaften, die nicht in der Struktur **ADRLIST** enthalten gel�scht. Zum Abrufen der aktuellen Gruppe von Eigenschaften f�r alle Empf�nger einer Nachricht [GetRecipientTable](imessage-getrecipienttable.md) aufrufen und Abrufen von allen Zeilen. Da ein **SRowSet** dieselbe Struktur wie eine **ADRLIST**ist, k�nnen Sie diese austauschbar verwenden.
  
 **ModifyRecipients** ersetzt alle Eintr�ge in der aktuellen Empf�ngerliste mit den Informationen, die auf den  _lpMods_, wenn keines der Flags im  _ulFlags_ -Parameter festgelegt werden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Sie das MODRECIP_MODIFY-Flag festlegen, ersetzt **ModifyRecipients** jedes Empf�ngers gesamte Zeile mit der zugeordneten Zeile in der [ADRLIST](adrlist.md) -Struktur in  _lpMods_�bergeben. Achten Sie darauf, dass alle Eigenschaften angeben, die ein Empf�nger haben sollen, unabh�ngig davon, ob sie ge�ndert haben, um zu verhindern, dass Sie versehentlich gel�scht wird.
  
Es folgen einige Regeln zum Festlegen der Eigenschaften der Empf�nger in der Struktur **ADRLIST**: 
  
- Verwenden Sie PT_NULL nicht als einen Eigenschaftentyp aus. **ModifyRecipients** gibt einen Fehler zur�ck, wenn dieser Wert auftreten. 
    
- Verwenden Sie PT_ERROR nicht als einen Eigenschaftentyp aus. **ModifyRecipients** wird dieser Wert ignoriert. 
    
- Fügen Sie die **PR_ROWID** -Eigenschaft für alle Empfänger in _UlFlags_legen Sie die MODRECIP_REMOVE oder MODRECIP_MODIFY-Flag. 
    
- Schlie�en Sie die **PR_ROWID** -Eigenschaft nicht f�r alle Empf�nger beim Festlegen der MODRECIP_ADD-Flag in  _ulFlags_ oder wenn Sie NULL in  _ulFlags_�bergeben.
    
Wenn Sie die **PR_ADDRTYPE** -Eigenschaft oder die **PR_EMAIL_ADDRESS** -Eigenschaft f�r einen Empf�nger und eine oder beide Eigenschaften sind inkonsistent mit den Adresstyp und die Adresse des Empf�ngers durch **PR_ENTRYID**bezeichnet, sind die Ergebnisse nicht definiert. D. h., gibt es drei M�glichkeiten, je nach Dienstanbieter:
  
- Die Nachricht wird an die Adresse, die von den Eigenschaften **PR_ADDRTYPE** und **PR_EMAIL_ADDRESS** beschriebenen �bermittelt werden. 
    
- Die Nachricht wird an den Empf�nger durch **PR_ENTRYID**identifizierten �bermittelt werden.
    
- Die Nachricht wird aufgrund der Mehrdeutigkeit der Adressinformationen unzustellbar deklariert werden.
    
Verwenden Sie die Regeln f�r die Zuweisung in [Verwalten von Arbeitsspeicher f�r ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md) beschriebenen Speicherzuordnung f�r die Empf�ngerliste. **ModifyRecipients** Freigabe nicht die Struktur **ADRLIST** noch keines der Unterstrukturen frei. Die Struktur **ADRLIST** und jede [SPropValue](spropvalue.md) Struktur m�ssen separat mithilfe der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) so, dass jeweils einzeln freigegeben werden zugeordnet werden. Wenn die Methode zus�tzlichen Speicherplatz f�r alle **SPropValue** Struktur erfordert, kann es die **SPropValue** -Struktur mit einer neuen ersetzen, die sp�ter mithilfe der [MAPIFreeBuffer](mapifreebuffer.md)freigegeben werden k�nnen. **SPropValue** Originalstruktur sollten auch mithilfe der **MAPIFreeBuffer**freigegeben werden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddRecipient  <br/> |MFCMAPI (engl.) verwendet die **IMessage::ModifyRecipients** -Methode, um einen neuen Empf�nger einer Nachricht hinzuf�gen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ADRENTRY](adrentry.md)
  
[ADRLIST](adrlist.md)
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IMAPISupport::Address](imapisupport-address.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

