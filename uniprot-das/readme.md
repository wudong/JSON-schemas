# UniProt DAS migration #

UniProt DAS will be retired by the end of this year; thus, we will provide some web services to replace the most common and used features in DAS. So far we plan to provide a sequence service, and a summary service.

## Sequence service ##
A JSON schema for UniProt sequences is available at https://github.com/ebi-uniprot/JSON-schemas/blob/master/uniprot-das/sequence.json. Requests to UniProt should support both acessions and identifiers. In a similar way, also UniParc sequences will be provided, the pattern for entry identifiers would be different though. Requests to UniPar should support UniParc identifiers.

Sequences will be provided in JSON, an additional XML format could be useful as well but not necessarily required.

DAS UniProt Sequence (http://www.ebi.ac.uk/das-srv/uniprot/das/uniprot/sequence?segment=A4_HUMAN)
```
<DASSEQUENCE>
	<SEQUENCE id="A4_HUMAN" start="1" stop="770" version="7dd43312cd29a262acdc0517230bc5ca" label="Amyloid beta A4 protein">
		MLPGLALLLLAAWTARALEVPTDGNAGLLAEPQIAMFCGRLNMHMNVQNGKWDSDPSGTKTCIDTKEGILQYCQEVYPELQITNVVEANQPVTIQNWCKRGRKQCKTHPHFVIPYRCLVGEFVSDALLVPDKCKFLHQERMDVCETHLHWHTVAKETCSEKSTNLHDYGMLLPCGIDKFRGVEFVCCPLAEESDNVDSADAEEDDSDVWWGGADTDYADGSEDKVVEVAEEEEVAEVEEEEADDDEDDEDGDEVEEEAEEPYEEATERTTSIATTTTTTTESVEEVVREVCSEQAETGPCRAMISRWYFDVTEGKCAPFFYGGCGGNRNNFDTEEYCMAVCGSAMSQSLLKTTQEPLARDPVKLPTTAASTPDAVDKYLETPGDENEHAHFQKAKERLEAKHRERMSQVMREWEEAERQAKNLPKADKKAVIQHFQEKVESLEQEAANERQQLVETHMARVEAMLNDRRRLALENYITALQAVPPRPRHVFNMLKKYVRAEQKDRQHTLKHFEHVRMVDPKKAAQIRSQVMTHLRVIYERMNQSLSLLYNVPAVAEEIQDEVDELLQKEQNYSDDVLANMISEPRISYGNDALMPSLTETKTTVELLPVNGEFSLDDLQPWHSFGADSVPANTENEVEPVDARPAADRGLTTRPGSGLTNIKTEEISEVKMDAEFRHDSGYEVHHQKLVFFAEDVGSNKGAIIGLMVGGVVIATVIVITLVMLKKKQYTSIHHGVVEVDAAVTPEERHLSKMQQNGYENPTYKFFEQMQN
	</SEQUENCE>
</DASSEQUENCE>
```

DAS UniParc Sequence (http://www.ebi.ac.uk/das-srv/uniprot/das/uniparc/sequence?segment=UPI0000125656)
```
<DASSEQUENCE>
	<SEQUENCE id="UPI0000125656" start="1" stop="69" version="cadb81119b2421b6e6be8cc4bcc1b5e8">
  		VVVLAGTNRPDVLDPALMRPGRFHRQIYTGPPYIKGRSSIFKVHLRPLKLDKSLNKDTLARKLAVLTPG
	</SEQUENCE>
</DASSEQUENCE>
```

## Summary service ##
The summary service provides a summary view of a protein entry. Summary features will be provided in XML. See an example at http://www.ebi.ac.uk/das-srv/uniprot/das/uniprot-summary/features?segment=P05067.
