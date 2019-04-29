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
ms.openlocfilehash: 0a9b88d762ca88cebd6d9acecf06db53a0b778f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423860"
---
# <a name="iablogonpreparerecips"></a>IABLogon::PrepareRecips

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor.
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameter

_ulFlags_
  
> in Eine Bitmaske von Flags, die den Texttyp in den zurückgegebenen Zeichenfolgen steuert. Das folgende Flag kann festgelegt werden:
    
  - MAPI_CACHE_ONLY: Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung die globale Adressliste (GAL) im Exchange-Cache-Modus zu öffnen und auf einen Eintrag in diesem Adressbuch aus dem Cache zuzugreifen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
_lpPropTagArray_
  
> in Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält, die die Eigenschaften anzeigen, die eine Aktualisierung erfordern, sofern vorhanden. Der _lpPropTagArray_ -Parameter kann NULL sein. 
    
_lpRecipList_
  
> in Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die die Empfängerliste enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängerliste wurde erfolgreich vorbereitet.
    
MAPI_E_NOT_FOUND 
  
> Mindestens einer der Empfänger im _lpRecipList_ -Parameter ist nicht vorhanden. 
    
## <a name="return-value"></a>Rückgabewert

Ein Client ruft die MAPI- [IAddrBook::P reparerecips](iaddrbook-preparerecips.md) -Methode auf, um eine Gruppe von Eigenschaften für einen oder mehrere Empfänger zu ändern oder neu anzuordnen. Die Empfänger sind möglicherweise Teil der Empfängerliste einer ausgehenden Nachricht. MAPI übergibt diesen Aufruf an die **IABLogon::P reparerecips** -Methode eines Adressbuch Anbieters. 
  
**IABLogon::P reparerecips** führt vier Hauptaufgaben aus: 
  
- Stellt sicher, dass alle Empfänger in der Adressliste, auf die durch den _lpRecipList_ -Parameter verwiesen wird, einen langfristigen Eintragsbezeichner aufweisen. 
    
- Stellt sicher, dass alle Empfänger über die Eigenschaften verfügen, die im Eigenschafts Wertarray angegeben sind, auf das durch den _lpPropTagArray_ -Parameter verwiesen wird. 
    
- Stellt sicher, dass die Eigenschaften aus dem Eigenschafts Wertarray vor allen anderen Eigenschaften angezeigt werden, die vor dem Aufruf vorhanden waren.
    
- Stellt sicher, dass die Reihenfolge der Eigenschaften in der [](adrentry.md) **ADRLIST** -Struktur der einzelnen Empfänger mit dem Wert des Eigenschaftswerts übereinstimmt. 
    
Die **** _lpRecipList_ -Parameter enthält eine **Miet** Struktur für jeden Empfänger. Jede **Miet** Struktur enthält ein Array von [SPropValue](spropvalue.md) -Strukturen, um die Eigenschaften des Empfängers zu beschreiben. Wenn **IABLogon::P reparerecips** zurückgibt, enthält das **SPropValue** -Strukturarray für jeden Empfänger die Eigenschaften aus dem _lpPropTagArray_ , gefolgt von den anderen Eigenschaften für den Empfänger. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung von **IABLogon::P reparerecips** umfasst das Platzieren von Eigenschaften in einer bestimmten Reihenfolge, das Abrufen von Eigenschaftswerten und das Konvertieren von kurzfristigen Eintrags Bezeichnern in langfristige Eintragsbezeichner. Die Eigenschaften, die im _lpPropTagArray_ -Parameter angefordert werden, müssen sich am Anfang des Eigenschafts Wertarrays befinden, das der **Miet** Struktur jedes Empfängers im _lpRecipList_ -Parameter zugeordnet ist. Wenn keine Werte für diese Eigenschaften vorhanden sind, öffnen Sie den zugeordneten Messagingbenutzer oder die zugehörige Verteilerliste unter Verwendung der Eintrags-ID, und rufen Sie die fehlenden Eigenschaftswerte ab. 
  
Ordnen Sie jede **SPropValue** -Struktur, die in _lpRecipList_ übergeben wird, separat zu, damit die Strukturen einzeln freigegeben werden können. Wenn Sie einen zusätzlichen Speicherplatz für eine **SPropValue** -Struktur zuweisen müssen, beispielsweise zum Speichern der Daten für eine String-Eigenschaft, verwenden Sie die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, um zusätzlichen Speicherplatz für das Array der vollständigen Eigenschaftswerte zuzuweisen. Verwenden Sie die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, um das ursprüngliche Eigenschaftswert Array freizugeben, und verwenden Sie dann die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, um zusätzlichen erforderlichen Arbeitsspeicher zuzuweisen. 
  
Gehen Sie folgendermaßen vor, um **IABLogon::P Reparerecips**zu implementieren:
  
1. Suchen Sie nach Einträgen im _lpPropTagArray_ -Parameter. Wenn das Eigenschaftswert Array leer ist, gibt es keine Aufgaben. Zurückgeben eines Erfolgs Werts. 
    
2. Verarbeiten Sie jeden Empfänger im _lpRecipList_ -Parameter. Für jeden Empfänger in der Liste gibt es ein Mitglied der **Miet** Struktur. Die folgenden Empfängertypen werden ignoriert: 
    
   - Empfänger ohne Eintragsbezeichner im **rgPropVals** -Element ihrer **Miet** Struktur (also nicht aufgelöste Empfänger). 
    
   - Empfänger mit einer Eintrags-ID, die nicht zu Ihrem Anbieter gehört. Diese Empfänger werden an einen anderen Adressbuchanbieter weitergeleitet.
    
3. Öffnen Sie den Empfänger, und rufen Sie die Eigenschaften ab, die bereits für den Empfänger festgelegt wurden.
    
4. Zusammenführen des in der _lpRecipList_ angegebenen Eigenschafts Wertarrays mit dem Array von Eigenschaften, die von GetProps zurückgegeben werden. **** Wenn die gleiche Eigenschaft in beiden Eigenschaften Arrays auftritt, verwenden Sie den Wert aus _lpRecipList_.
    
5. Wenn das _lpRecipList_ -Eigenschaftenwert Array groß genug ist, um alle erforderlichen Eigenschaften zu speichern, ersetzen Sie es durch das zusammengeführte Array. Wenn das _lpRecipList_ -Eigenschaftswert-Array nicht groß genug ist, ersetzen Sie es durch ein neu zugeordnetes Array. Stellen Sie sicher, dass das neue Array in jedem seiner **cValues** -Mitglieder über einen aktualisierten Wert verfügt. 
    
6. Wenn Sie eine oder mehrere der Eigenschaften im _lpPropTagArray_ -Parameter nicht erkennen, legen Sie den Eigenschaftentyp in der **Miet** Struktur des Empfängers auf PT_ERROR und den Eigenschaftswert entweder auf MAPI_E_NOT_FOUND oder auf einen anderen Wert fest, der mehr ein bestimmter Grund für die Nichtverfügbarkeit der Eigenschaft. Weitere Informationen zu PT_ERROR finden Sie unter [Property Types](property-types.md).
    
> [!NOTE]
> Ordnen Sie die **ADRLIST** -Struktur, die an IABLogon übergeben wird, nie neu zu **::P reparerecips** , oder ändern Sie die Anzahl der Einträge. 
  
## <a name="see-also"></a>Siehe auch

- [ADRLIST](adrlist.md)
- [IMAPIProp::GetProps](imapiprop-getprops.md)
- [Kanonische PidTagEntryId-Eigenschaft](pidtagentryid-canonical-property.md)
- [SPropValue](spropvalue.md)
- [IABLogon : IUnknown](iablogoniunknown.md)

