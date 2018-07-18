---
title: Lesen und Analysieren eines Serienmusters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 75113097-b3ae-4d20-9796-85c62a592ef0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 694d63165bb820ffef1a29d1646861435fc4ed26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791870"
---
# <a name="read-and-parse-a-recurrence-pattern"></a>Lesen und Analysieren eines Serienmusters
  
**Betrifft**: Outlook 
  
MAPI kann zum Lesen und Analysieren eines Serienmusters, das für einen Termin verwendet werden.
  
Informationen zum Herunterladen, anzeigen, und führen Sie den Code aus dem MFCMAPI (engl.) Anwendung-Projekt verwiesen, die in diesem Thema finden Sie unter [Installieren der Beispiele in diesem Abschnitt verwendet](how-to-install-the-samples-used-in-this-section.md).

### <a name="to-parse-a-recurrence-blob"></a>Analysieren einen Serienblob

1. Öffnen Sie ein Terminelement. Informationen zum Öffnen einer Nachricht finden Sie unter [Öffnen einer Nachricht](opening-a-message.md).
    
2. Rufen Sie die benannte Eigenschaft **DispidApptRecur** ([PidLidAppointmentRecur kanonische-Eigenschaft](pidlidappointmentrecur-canonical-property.md)) ab. Informationen zum Abrufen von benannten Eigenschaften finden Sie unter [MAPI-Eigenschaften mit dem Namen](mapi-named-properties.md).
    
3. Führen Sie die Anweisungen in [[MS-OXOCAL]](http://msdn.microsoft.com/en-us/library/cc425490%28EXCHG.80%29.aspx) die Termin Serie Muster-Struktur zu lesen. 
    
Die MFCMAPI (engl.)-Referenz-Anwendung veranschaulicht den letzten Schritt mit der `BinToAppointmentRecurrencePatternStruct` Funktion in der Quelldatei InterpretProp2.cpp des Projekts MFCMAPI (engl.). Die `BinToAppointmentRecurrencePatternStruct` Funktion einen Zeiger auf einem Puffer im Arbeitsspeicher als Parameter akzeptiert. Die Anwendung MFCMAPI (engl.) abruft dieses Puffers durch Zuordnen von der **DispidApptRecur** -Eigenschaft auf ein Eigenschaftentag klicken Sie dann mit der durch den Wert der Eigenschaft mithilfe der Methode [IMAPIProp::GetProps](imapiprop-getprops.md) anfordern. Wenn die Eigenschaft rufen Sie mithilfe der Methode **GetProps** zu groß ist, wird MFCMAPI (engl.) eine Stream-Schnittstelle zum Abrufen der Eigenschaft mithilfe der Methode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) geöffnet. Klicken Sie dann die MFCMAPI (engl.) Anwendung liest die Daten aus dem Datenstrom Puffer zu erstellen. 
  
Informationen über das Format des Puffers finden Sie unter der [PidLidAppointmentRecur kanonische-Eigenschaft](pidlidappointmentrecur-canonical-property.md). Der Großteil der Daten im Puffer besteht aus Feldern eine festgelegte Anzahl von Bytes, die nach dem anderen gelesen werden muss. Einige Felder sind vorhanden, nur, wenn andere Felder bestimmte Werte enthalten, und die Größe der einige Felder kann der Wert der anderen Felder abhängen. Analysieren den Puffer zum Lesen der verschiedenen Felder umfasst viele Buchhaltung. MFCMAPI (engl.) verwendet wird, als interne Hilfsklasse, die mit dem Namen `CBinaryParser` dieser Buchhaltung kapseln. Beispielsweise die `CBinaryParser::GetDWORD` Funktion überprüft, ob genügend Bytes im Puffer zum Lesen von eines DWORD-Wert bleiben, und klicken Sie dann den Wert liest und die Zeiger aktualisiert. 
  
Nachdem Sie der Puffer in einer Struktur analysiert wurde, verwendet die Anwendung MFCMAPI (engl.) der `AppointmentRecurrencePatternStructToString` Funktion zum Konvertieren der Struktur in eine Zeichenfolge, die für den Benutzer anzuzeigen. Dies ist nicht dieselbe Zeichenfolge, die Outlook angezeigt würden, die jedoch ist stattdessen eine unformatierte Ansicht der Daten auf denen Outlook seine Logik aufbaut. 
  
Es ist möglich, einen Puffer auftreten, der beschädigte Daten oder mehr Daten als benötigt werden, um ein Serienmuster codieren enthält. Um diese Szenarien zu identifizieren, verfolgt die Anwendung MFCMAPI (engl.) über wie viele Daten erfolgreich analysiert wurde und wie viel im Puffer bleibt. Wenn Daten im Puffer bleibt, nachdem die Analyse abgeschlossen ist, einschließlich der MFCMAPI (engl.) dieses "Junk-e-Daten" in der Struktur, damit er untersucht werden kann.
  
Im folgenden finden Sie eine vollständige Liste der der `BinToAppointmentRecurrencePatternStruct` Funktion. 
  
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

- [Erstellen von Outlook 2007-Elementen mithilfe von MAPI](http://msdn.microsoft.com/en-us/library/cc678348%28office.12%29.aspx)

