---
title: IABLogonPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.PrepareRecips
api_type:
- COM
ms.assetid: 3c1845ea-e291-4855-9afd-51d2c64d7e85
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c42077528a4f7227321d8f987cc5dd0ccd4c966c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589742"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bereitet eine Empfängerliste zur späteren Verwendung von messaging-System.
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> [in] Eine Bitmaske aus Flags, die den Typ des Texts in der zurückgegebenen Zeichenfolge steuert. Das folgende Flag kann festgelegt werden:
    
  - MAPI_CACHE_ONLY: Verwenden Sie nur das Offlineadressbuch namensauflösung ausführen. Dieses Kennzeichen können Sie beispielsweise ermöglichen einer Clientanwendung zum Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus und Zugreifen auf einen Eintrag in diesem Adressbuch aus dem Cache ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
_lpPropTagArray_
  
> [in] Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags, die die Eigenschaften, die aktualisieren enthält angeben, wenn erfordern. Der Parameter _LpPropTagArray_ kann NULL sein. 
    
_lpRecipList_
  
> [in] Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die die Empfängerliste enthält. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Empfängerliste wurde erfolgreich vorbereitet.
    
MAPI_E_NOT_FOUND 
  
> Eine oder mehrere Empfänger in der _LpRecipList_ -Parameter sind nicht vorhanden. 
    
## <a name="return-value"></a>R�ckgabewert

Ein Client Ruft die MAPI- [IAddrBook::PrepareRecips](iaddrbook-preparerecips.md) -Methode zum Ändern oder neu anordnen eine Reihe von Eigenschaften für einen oder mehrere Empfänger an. Der Empfänger können oder möglicherweise nicht Teil der Liste der Empfänger von ausgehenden Nachrichten. MAPI überträgt dieses Anrufs an eine Adressbuchanbieter **IABLogon::PrepareRecips** -Methode. 
  
**IABLogon::PrepareRecips** werden die vier Wichtigste Aufgaben ausgeführt: 
  
- Stellt sicher, dass alle Empfänger in der Adressliste verwiesen durch den Parameter _LpRecipList_ langfristige Eintrags-ID verfügen. 
    
- Stellt sicher, dass alle Empfänger die Eigenschaften den Wert Array-Eigenschaft auf das durch den Parameter _LpPropTagArray_ angegeben haben. 
    
- Stellt sicher, dass die Eigenschaften aus dem Array der Eigenschaft Wert vor alle anderen Eigenschaften werden angezeigt, die vor dem Aufruf vorhanden waren.
    
- Stellt sicher, dass die Reihenfolge der Eigenschaften des Empfängers [ADRENTRY](adrentry.md) Struktur in der Struktur **ADRLIST** Array der Wert-Eigenschaft identisch ist. 
    
Die **ADRENTRY** -Struktur in der _LpRecipList_ -Parameter enthält eine **ADRENTRY** -Struktur für jeden Empfänger. Jede **ADRENTRY** -Datenstruktur enthält ein Array von [SPropValue](spropvalue.md) -Strukturen, um die Eigenschaften des Empfängers zu beschreiben. Wenn **IABLogon::PrepareRecips** zurückgegeben wird, enthält das **SPropValue** -Struktur-Array für jeden Empfänger die Eigenschaften aus der _LpPropTagArray_ , gefolgt von den anderen Eigenschaften für den Empfänger. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Implementieren von **IABLogon::PrepareRecips** umfasst Eigenschaften in einer bestimmten Reihenfolge einfügen, Abrufen von Eigenschaftswerten und kurzfristige-Eintragsbezeichner in langfristige-Eintragsbezeichner konvertieren. Die Eigenschaften, die im Parameter _LpPropTagArray_ angefordert werden, müssen am Anfang des Arrays der Eigenschaft Wert des Empfängers **ADRENTRY** Struktur im Parameter _LpRecipList_ zugeordnet sein. Wenn Werte für diese Eigenschaften nicht vorhanden sind, öffnen Sie die zugeordnete messaging Benutzer oder eine Verteilergruppe der angegebenen Liste mithilfe von dessen Eintrags-ID und abgerufen Sie fehlenden Werte. 
  
Ordnen Sie jede **SPropValue** Struktur übergebenen _LpRecipList_ separat, damit die Strukturen einzeln freigegeben werden können. Wenn Sie zusätzlichen Speicherplatz für alle **SPropValue** -Struktur zuweisen müssen, beispielsweise zum Speichern der Daten für eine Zeichenfolgeneigenschaft verwenden Sie die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) zusätzlichen Speicherplatz für Wertearray vollständige-Eigenschaft zugewiesen werden. Verwenden Sie die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion das ursprünglichen Eigenschaft Wertearray frei, und klicken Sie dann verwenden Sie die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, um alle zusätzlichen Speicher zuweisen, der erforderlich ist. 
  
Um **IABLogon::PrepareRecips**implementieren möchten, verwenden Sie die folgende Schritte aus:
  
1. Überprüfen Sie die Einträge in der _LpPropTagArray_ -Parameter. Wenn das Wertearray-Eigenschaft leer ist, ist gibt es keine Arbeit. Einen Erfolgswert zurück. 
    
2. Verarbeiten Sie jeden Empfänger in der _LpRecipList_ -Parameter. Es ist ein Mitglied der **ADRENTRY** -Struktur für jeden Empfänger in der Liste aus. Ignorieren Sie die folgenden Typen von Empfängern: 
    
   - Empfänger ohne Bezeichner Eintrag im **RgPropVals** Mitglied ihrer **ADRENTRY** -Struktur (d. h., nicht aufgelösten Empfänger). 
    
   - Empfänger mit einem Eintrag Bezeichner, der nicht zu Ihrem Anbieter gehört. Diese Empfänger werden an eine andere Adressbuchanbieter übergeben werden.
    
3. Öffnen Sie den Empfänger und Abrufen der Eigenschaften, die bereits für den Empfänger festgelegt sind.
    
4. Zusammenführen Sie angegebene, in der _LpRecipList_ mit dem Array von Eigenschaften von **GetProps**zurückgegebenen Array der Eigenschaft Wert. Wenn die gleiche Eigenschaft in beiden Arrays Eigenschaft auftritt, verwenden Sie den Wert von _LpRecipList_.
    
5. Wenn _LpRecipList_ -Eigenschaft Wertearray groß genug, um alle erforderlichen Eigenschaften enthalten ist, ersetzen Sie ihn nur durch das verbundene Array. Wenn Wertearray der _LpRecipList_ -Eigenschaft nicht groß genug ist, ersetzen Sie ihn durch eine neu zugeordnete Array. Stellen Sie sicher, dass für das neue Array einen aktualisierten Wert in den einzelnen Membern **cValues** ist. 
    
6. Wenn Sie eine oder mehrere der Eigenschaften im _LpPropTagArray_ -Parameter nicht erkennen, legen Sie den Eigenschaftstyp in der Aufgabenliste des Empfängers zu PT_ERROR und den Wert der Eigenschaft um MAPI_E_NOT_FOUND oder auf einen anderen Wert, der eine einheitliche **ADRENTRY** -Struktur bestimmte Grund für den Ausfall der-Eigenschaft. Informationen zu PT_ERROR finden Sie unter [Eigenschaftentypen](property-types.md).
    
> [!NOTE]
> Nie Zuordnen der **ADRLIST** -Struktur, die in **IABLogon::PrepareRecips** übergeben wird, oder ändern Sie die Anzahl der Einträge. 
  
## <a name="see-also"></a>Siehe auch

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

