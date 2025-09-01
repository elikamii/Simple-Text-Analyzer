def analyze_text(text):
    """
    Analyzes a given text to return word count, character count, line count, and average word length.
    """
    if not isinstance(text, str):
        return

        avg_word_length = sum(len(word) for word in words) / word_count
        
    return {
        "word_count": word_count,
        "character_count": char_count,
        "line_count": line_count,
        "average_word_length": round(avg_word_length, 2)
    }

if __name__ == "__main__":
    sample_text = """This is a simple text.
It has multiple lines to analyze.
Let's see the results!"""
    analysis_results = analyze_text(sample_text)
    print("--- Text Analysis Results ---")
    for key, value in analysis_results.items():
        print(f"{key.replace('_', ' ').title()}: {value}")
