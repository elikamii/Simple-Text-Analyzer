def analyze_text(text):
    """
    Analyzes a given text to return word count, character count, and average word length.
    """
    if not isinstance(text, str):
        return "Error: Input must be a string."

    words = text.split()
    word_count = len(words)
    char_count = len(text)
    
    if word_count == 0:
        avg_word_length = 0
    else:
        avg_word_length = sum(len(word) for word in words) / word_count
        
    return {
        "word_count": word_count,
        "character_count": char_count,
        "average_word_length": round(avg_word_length, 2)
    }

if __name__ == "__main__":
    sample_text = "This is a simple text to analyze."
    analysis_results = analyze_text(sample_text)
    print("--- Text Analysis Results ---")
    for key, value in analysis_results.items():
        print(f"{key.replace('_', ' ').title()}: {value}")
