---
title: Lesen und Analysieren eines Serienmusters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 75113097-b3ae-4d20-9796-85c62a592ef0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6c5b7addd9a62e8f87bee1435f1c73ae61e34333
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561691"
---
# <a name="read-and-parse-a-recurrence-pattern"></a>Lesen und Analysieren eines Serienmusters
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI kann zum Lesen und Analysieren eines Serienmusters für einen Termin verwendet werden.
  
Informationen zum Herunterladen, Anzeigen und Ausführen des Codes aus dem MFCMAPI-Anwendungsprojekt, auf das in diesem Thema verwiesen wird, finden Sie unter [Installieren der in diesem Abschnitt verwendeten Beispiele.](how-to-install-the-samples-used-in-this-section.md)

### <a name="to-parse-a-recurrence-blob"></a>So analysieren Sie ein Serienblob

1. Öffnen Sie ein Terminelement. Informationen zum Öffnen einer Nachricht finden Sie unter ["Öffnen einer Nachricht".](opening-a-message.md)
    
2. Abrufen der benannten Eigenschaft **dispidApptRecur** ([PidLidAppointmentRecur (kanonische Eigenschaft).](pidlidappointmentrecur-canonical-property.md) Informationen zum Abrufen benannter Eigenschaften finden Sie unter [MAPI Named Properties](mapi-named-properties.md).
    
3. Befolgen Sie die Anleitung in [[MS-OXOCAL],](https://msdn.microsoft.com/library/cc425490%28EXCHG.80%29.aspx) um die Struktur des Terminserienmusters zu lesen. 
    
Die MFCMAPI-Referenzanwendung veranschaulicht den letzten Schritt mit der  `BinToAppointmentRecurrencePatternStruct` Funktion in der Quelldatei "InterpretProp2.cpp" des MFCMapi-Projekts. Die  `BinToAppointmentRecurrencePatternStruct` Funktion verwendet einen Zeiger auf einen Puffer im Speicher als Parameter. Die MFCMAPI-Anwendung ruft diesen Puffer ab, indem sie zuerst die benannte Eigenschaft **"dispidApptRecur"** einem Eigenschaftstag zuweist und dann den Wert der Eigenschaft mithilfe der [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) anfordert. Wenn die Eigenschaft zu groß ist, um sie mithilfe der **GetProps-Methode** abzurufen, öffnet MFCMAPI eine Streamschnittstelle, um die Eigenschaft mithilfe der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) abzurufen. Die MFCMAPI-Anwendung liest dann die Daten aus dem Datenstrom, um den Puffer zu erstellen. 
  
Informationen zum Format des Puffers finden Sie unter der [kanonischen PidLidAppointmentRecur-Eigenschaft.](pidlidappointmentrecur-canonical-property.md) Der Großteil der Daten im Puffer besteht aus Feldern mit einer festen Anzahl von Bytes, die nacheinander gelesen werden müssen. Einige Felder sind nur vorhanden, wenn andere Felder bestimmte Werte enthalten, und die Größe einiger Felder kann vom Wert anderer Felder abhängen. Das Analysieren des Puffers zum Lesen der verschiedenen Felder erfordert viel Buchführung. MFCMAPI verwendet eine interne  `CBinaryParser` Hilfsklasse, die benannt ist, um diese Buchführung zu kapseln. Beispielsweise überprüft die  `CBinaryParser::GetDWORD` Funktion, ob genügend Bytes im Puffer verbleiben, um einen DWORD-Wert zu lesen, und liest dann den Wert und aktualisiert die Zeiger. 
  
Nachdem der Puffer in eine Struktur analysiert wurde, verwendet die MFCMAPI-Anwendung die  `AppointmentRecurrencePatternStructToString` Funktion, um die Struktur in eine Zeichenfolge zu konvertieren, die dem Benutzer angezeigt werden soll. Dies ist nicht dieselbe Zeichenfolge, die Outlook anzeigen würde, sondern eine unformatierte Ansicht der Daten, auf denen Outlook ihre Logik erstellt. 
  
Es ist möglich, auf einen Puffer zu treffen, der entweder beschädigte Daten oder mehr Daten enthält, als zum Codieren eines Serienmusters erforderlich sind. Um diese Szenarien zu identifizieren, verfolgt die MFCMAPI-Anwendung, wie viele Daten erfolgreich analysiert wurden und wie viel im Puffer verbleibt. Wenn Daten im Puffer verbleiben, nachdem die Analyse abgeschlossen ist, schließt MFCMAPI diese "Junk-Daten" in die Struktur ein, damit sie untersucht werden können.
  
Es folgt die vollständige Auflistung der  `BinToAppointmentRecurrencePatternStruct` Funktion. 
  
```cpp
AppointmentRecurrencePatternStruct* BinToAppointmentRecurrencePatternStruct(ULONG cbBin, LPBYTE lpBin)
{
   if (!lpBin) return NULL;
   AppointmentRecurrencePatternStruct arpPattern = {0};
   CBinaryParser Parser(cbBin,lpBin);
   size_t cbBinRead = 0;
   arpPattern.RecurrencePattern = BinToRecurrencePatternStruct(cbBin,lpBin,&cbBinRead);
   Parser.Advance(cbBinRead);
   Parser.GetDWORD(&arpPattern.ReaderVersion2);
   Parser.GetDWORD(&arpPattern.WriterVersion2);
   Parser.GetDWORD(&arpPattern.StartTimeOffset);
   Parser.GetDWORD(&arpPattern.EndTimeOffset);
   Parser.GetWORD(&arpPattern.ExceptionCount);
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions)
   {
      arpPattern.ExceptionInfo = new ExceptionInfoStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExceptionInfo)
      {
         memset(arpPattern.ExceptionInfo,0,sizeof(ExceptionInfoStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].StartDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].EndDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].OriginalStartDate);
            Parser.GetWORD(&arpPattern.ExceptionInfo[i].OverrideFlags);
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength2);
               if (arpPattern.ExceptionInfo[i].SubjectLength2 && arpPattern.ExceptionInfo[i].SubjectLength2 + 1 
                  == arpPattern.ExceptionInfo[i].SubjectLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].SubjectLength2,&arpPattern.ExceptionInfo[i].Subject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_MEETINGTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].MeetingType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDERDELTA)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderDelta);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDER)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderSet);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength2);
               if (arpPattern.ExceptionInfo[i].LocationLength2 && arpPattern.ExceptionInfo[i].LocationLength2 
                  + 1 == arpPattern.ExceptionInfo[i].LocationLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].LocationLength2,&arpPattern.ExceptionInfo[i].Location);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_BUSYSTATUS)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].BusyStatus);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_ATTACHMENT)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].Attachment);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].SubType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_APPTCOLOR)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].AppointmentColor);
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock1Size);
   if (arpPattern.ReservedBlock1Size && arpPattern.ReservedBlock1Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock1Size,&arpPattern.ReservedBlock1);
   }
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions &&
      arpPattern.ExceptionInfo)
   {
      arpPattern.ExtendedException = new ExtendedExceptionStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExtendedException)
      {
         memset(arpPattern.ExtendedException,0,sizeof(ExtendedExceptionStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            if (arpPattern.WriterVersion2 >= 0x0003009)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightValue);
               if (arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize > sizeof(DWORD))
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize 
                     - sizeof(DWORD),&arpPattern.ExtendedException[i].ChangeHighlight.Reserved);
               }
            }
            Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE1Size);
            if (arpPattern.ExtendedException[i].ReservedBlockEE1Size &&
                arpPattern.ExtendedException[i].ReservedBlockEE1Size < _MaxReservedBlock)
            {
               Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE1Size,&arpPattern.ExtendedException[i].ReservedBlockEE1);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].StartDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].EndDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].OriginalStartDate);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharSubjectLength);
               if (arpPattern.ExtendedException[i].WideCharSubjectLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharSubjectLength,&arpPattern.ExtendedException[i].WideCharSubject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharLocationLength);
               if (arpPattern.ExtendedException[i].WideCharLocationLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharLocationLength,&arpPattern.ExtendedException[i].WideCharLocation);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE2Size);
               if (arpPattern.ExtendedException[i].ReservedBlockEE2Size && arpPattern.ExtendedException[i].ReservedBlockEE2Size < _MaxReservedBlock)
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE2Size,&arpPattern.ExtendedException[i].ReservedBlockEE2);
               }
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock2Size);
   if (arpPattern.ReservedBlock2Size && arpPattern.ReservedBlock2Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock2Size,&arpPattern.ReservedBlock2);
   }
   // Junk data remains.
   if (Parser.RemainingBytes() > 0)
   {
      arpPattern.JunkDataSize = Parser.RemainingBytes();
      Parser.GetBYTES(arpPattern.JunkDataSize,&arpPattern.JunkData);
   }
   AppointmentRecurrencePatternStruct* parpPattern = new AppointmentRecurrencePatternStruct;
   if (parpPattern)
   {
      *parpPattern = arpPattern;
   }
   return parpPattern;
}

```

## <a name="see-also"></a>Siehe auch

- [Verwenden von MAPI zum Erstellen von Outlook 2007-Elementen](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

